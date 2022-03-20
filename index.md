# meme sharing
# Kia ora ao!
HELLO! 你好！

Welcome to my website!!!

![hellogif](https://c.tenor.com/jFpA5woxTmAAAAAC/hey-friend-penguin.gif)
## *5 Things About Me*
1. I'm an international student at the [University of Auckland](https://www.auckland.ac.nz/en.html?gclid=CjwKCAiAt9z-BRBCEiwA_bWv-NiyadpTq90gc2Y925iux3_MtVVwn1KRq3pRZmWVK5zqLy5aTtWSxBoCerAQAvD_BwE).
2. Current location: [Beijing](https://www.google.com/maps/place/Beijing,+China/@39.9375346,115.837023,9z/data=!3m1!4b1!4m5!3m4!1s0x35f05296e7142cb9:0xb9625620af0fa98a!8m2!3d39.904211!4d116.407395)🇨🇳
3. Taking Finance ✖️ Statistics 
4. Three of my favourite things: dance, photography, and bubble tea👍🏻
5. My little wish: COVID-19 will end as soon as possible🙏🏻

## *About Assignment 1...*
Here is the meme I created for the first assignment using the R package [{magick}](https://cran.r-project.org/web/packages/magick/vignettes/intro.html).
![my_meme](https://user-images.githubusercontent.com/101943620/159171573-e922933d-c686-4891-9d8b-69f6266c33a8.png)
### story about this meme
I made this spongebob meme with an idea came up when I was watching recordings. 

Students might feel a bit stressed out during the lectures, but wouldn't it be cool to learn how to make a meme with R Studio in class?


I chose [Spongebob](https://en.wikipedia.org/wiki/SpongeBob_SquarePants) as the character in my meme because I just watched this animation recently.

### R code about this meme
Also, below is the `R` code I used to create my first meme in STATS 220.
```
library(magick)

#image one
tired <- image_read("https://pyxis.nymag.com/v1/imgs/e1e/6b7/e7e202e97398fd64f6f9b6c6d13a526234-tired-spongebob.rhorizontal.w700.jpg") %>%
  image_scale(700) %>%
  image_annotate(text = "studying in the library",
                 size = 50,
                 gravity = "south",
                 color = "#000000",
                 boxcolor = "#ffffff",
                 font = "sans")

#image two
happy <- image_read("https://images4.fanpop.com/image/photos/19600000/SpongeBob-Photo-happy-square-sponge-19621591-640-360.jpg") %>%
  image_scale(700) %>%
  image_annotate(text = "making memes \n in the library",
                 size = 50,
                 gravity = "south",
                 color = "#000000",
                 boxcolor = "#ffffff",
                 font = "sans")

meme_vector <- image_append(c(tired, happy), stack = TRUE)

image_write(meme_vector, "my_meme.png")
```

Hope you like my meme and idea!!!😊
