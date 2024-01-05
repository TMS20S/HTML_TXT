<html>
<head>
  <style>
    $gs: 2em;
    $ms: 2*$gs;
    $c: fuchsia;
    
    body, div { display: grid }
    
    body {
    	margin: 0;
    	height: 100vh;
    	background: #262626
    }
    
    div {
    	place-self: center;
    	overflow: hidden;
    	border-radius: 7px;
    	box-shadow: 2px 2px 5px #141414;
    	
    	&::before, &::after {
    		--pattern: 
    			linear-gradient(90deg, #000, #{$c}, #000);
    		grid-area: 1/ 1;
    		padding: 45vmin;
    		background: 
    			linear-gradient(rgba($c, .47), #000), 
    			linear-gradient($c, rgba(#000, .47)), 
    			var(--pattern) 0 0/ #{$gs $gs};
    		background-blend-mode: screen, multiply;
    		filter: contrast(35) contrast(.65);
    		content: ''
    	}
    	
    	&::after {
    		--pattern: 
    			radial-gradient(#{$c}, #000 71%);
    		--mask: 
    			repeating-conic-gradient(
    					red 0% 25%, transparent 0% 50%) 
    				0 0/ #{$ms $ms};
    		-webkit-mask: var(--mask);
    						mask: var(--mask)
    	}
    }
</style>
</head>
<body>
  <div>
    
  </div>
</body>
</html>
