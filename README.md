Github Badge
============

A small github badge made with jQuery.
It was inpired by the [github social coding](http://githubbadge.appspot.com/)
badge (but has fewer bells and whistles). This may cause client side users to
exceed their github api usage limit.


Example:
--------

![Github Badge Screenshot](http://welbornprod.com/dl/img/github-badge.png)

Usage:
------

```html
<!-- Include all necessary files. -->
<link type='text/css' rel='stylesheet' href='github-badge.css'>
<script type='text/javascript' src='https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js'></script>
<script type='text/javascript' src='github-badge.js'></script>

<!-- Create a div to put the badge in. -->
<div id="github-badge-wrapper">
</div>

<!-- Fill it with the badge on document.ready -->
<script type='text/javascript'>
    $(document).ready(function () {
        github_badge.build_badge(
            // Include your own github user name here:
            'myusername',
            function success(div) {
                // div is an element containing the badge.
                $('#github-badge-wrapper').html(div);
            },
            function error(error_message) {
                // Somewhere down the line it failed, so don't show the div.
                console.log('Cannot build github badge: ' + error_message);
                $('#github-badge-wrapper').css({display: 'none'});
            }
        );
    });
</script>
```
