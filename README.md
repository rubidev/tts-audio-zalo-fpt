<script src="https://stc-ai-developers.zdn.vn/js/hls.js"></script>
<script>document.addEventListener('DOMContentLoaded', () => {
	const source =  document.querySelector('audio').querySelector('source').getAttribute('src');
	const audio = document.querySelector('audio');
	
	// For more options see: https://github.com/sampotts/plyr/#options
	// captions.update is required for captions to work with hls.js
	
	if (!Hls.isSupported()) {
		audio.src = source;
	} else {
		// For more Hls.js options, see https://github.com/dailymotion/hls.js
		const hls = new Hls();
		hls.loadSource(source);
		hls.attachMedia(audio);
		window.hls = hls;
		
		// Handle changing captions
		
	}
	
	// Expose player so it can be used from the console
	//window.player = player;
});
</script>
