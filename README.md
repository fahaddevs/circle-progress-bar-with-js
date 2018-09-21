# circle-progress-bar-with-js
It's a circle progress bar.

### Required js file
*<script src="jquery-3.3.1.min.js"></script>
*<script src="circle-progress.min.js"></script>


``` html
    <script src="jquery-3.3.1.min.js"></script>
    <script src="circle-progress.min.js"></script>
    <div class="skill-part">
        <div class="skill-item">
            <div class="first circle" data-skill-level="95">
                <h2></h2>
                <span class="sk-name">wordpress</span>
            </div>
        </div>
        <div class="skill-item">
            <div class="second circle" data-skill-level="80">
                <h2></h2>
                <span class="sk-name">user research</span>
            </div>
        </div>
        <div class="skill-item">
            <div class="third circle" data-skill-level="70">
                <h2></h2>
                <span class="sk-name">HTML &amp; CSS</span>
            </div>
        </div>
        <div class="skill-item">
            <div class="fourth circle" data-skill-level="90">
                <h2></h2>
                <span class="sk-name">Javascript</span>
            </div>
        </div>
    </div>
    <script>
        (function($){
    'use strict';   

   jQuery(document).ready(function($){
    
 
        // skill circle progress bar
        var skillLevel1 = $('.skill-item .first').data('skill-level');
        var skillLevel2 = $('.skill-item .second').data('skill-level');
        var skillLevel3 = $('.skill-item .third').data('skill-level');
        var skillLevel4 = $('.skill-item .fourth').data('skill-level');
        //first.circle
        $('.first.circle').circleProgress({
        value: '0.' + skillLevel1,
        size: 110,
        emptyFill: "#f2f2f2",
        fill: {
            color: "#39b54a"
        }
        }).on('circle-animation-progress', function(event, progress) {
        $(this).find('h2').html(Math.round(95 * progress) + '<span>%</span>');
        });

        //second.circle
        $('.second.circle').circleProgress({
        value: '0.' + skillLevel2,
        size: 110,
        emptyFill: "#f2f2f2",
        fill: {
            color: "#f26522"
        }
        }).on('circle-animation-progress', function(event, progress) {
        $(this).find('h2').html(Math.round(skillLevel2 * progress) + '<i>%</i>');
        });

        //third.circle
        $('.third.circle').circleProgress({
        value: '0.' + skillLevel3,
        size: 110,
        emptyFill: "#f2f2f2",
        fill: {
            color: "#6e41ff"
        }
        }).on('circle-animation-progress', function(event, progress) {
        $(this).find('h2').html(Math.round(70 * progress) + '<span>%</span>');
        });

        //fourth.circle
        $('.fourth.circle').circleProgress({
        value: '0.' + skillLevel4,
        size: 110,
        emptyFill: "#f2f2f2",
        fill: {
            color: "#ec008c"
        }
        }).on('circle-animation-progress', function(event, progress) {
        $(this).find('h2').html(Math.round(90 * progress) + '<span>%</span>');
        });

        });
    
    })(jQuery);	 
    </script>
```
