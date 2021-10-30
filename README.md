# NumberCounter
number counter using JS HTML BootStrap
```
                                                                                               
RRRRRRRRRRRRRRRRR             OOOOOOOOO                  CCCCCCCCCCCCC     KKKKKKKKK    KKKKKKK
R::::::::::::::::R          OO:::::::::OO             CCC::::::::::::C     K:::::::K    K:::::K
R::::::RRRRRR:::::R       OO:::::::::::::OO         CC:::::::::::::::C     K:::::::K    K:::::K
RR:::::R     R:::::R     O:::::::OOO:::::::O       C:::::CCCCCCCC::::C     K:::::::K   K::::::K
  R::::R     R:::::R     O::::::O   O::::::O      C:::::C       CCCCCC     KK::::::K  K:::::KKK
  R::::R     R:::::R     O:::::O     O:::::O     C:::::C                     K:::::K K:::::K   
  R::::RRRRRR:::::R      O:::::O     O:::::O     C:::::C                     K::::::K:::::K    
  R:::::::::::::RR       O:::::O     O:::::O     C:::::C                     K:::::::::::K     
  R::::RRRRRR:::::R      O:::::O     O:::::O     C:::::C                     K:::::::::::K     
  R::::R     R:::::R     O:::::O     O:::::O     C:::::C                     K::::::K:::::K    
  R::::R     R:::::R     O:::::O     O:::::O     C:::::C                     K:::::K K:::::K   
  R::::R     R:::::R     O::::::O   O::::::O      C:::::C       CCCCCC     KK::::::K  K:::::KKK
RR:::::R     R:::::R     O:::::::OOO:::::::O       C:::::CCCCCCCC::::C     K:::::::K   K::::::K
R::::::R     R:::::R      OO:::::::::::::OO         CC:::::::::::::::C     K:::::::K    K:::::K
R::::::R     R:::::R        OO:::::::::OO             CCC::::::::::::C     K:::::::K    K:::::K
RRRRRRRR     RRRRRRR          OOOOOOOOO                  CCCCCCCCCCCCC     KKKKKKKKK    KKKKKKK
                                                                                                                                                                                        
```

# NumberCounter
Download and Run

## JS Code

```javascript
  //number
    $(document).ready(function () {

        $('.counter').each(function () {
            $(this).prop('Counter', 0).animate({
                Counter: $(this).text()
            }, {
                duration: 4000,
                easing: 'swing',
                step: function (now) {
                    $(this).text(Math.ceil(now));
                }
            });
        });

    });

    //decimals number
    $("#decimals").animateNumber(
        {
            number: 2500,
            numberStep: function (now, tween) {
                // see http://stackoverflow.com/a/14428340
                var formatted = now.toFixed(2).replace(/(\d)(?=(\d{3})+\.)/g, "$1,");
                $(tween.elem).text("$" + formatted);
            }
        },
        4000
    );

```
