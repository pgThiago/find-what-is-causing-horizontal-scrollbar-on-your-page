# Find what is causing horizontal scrollbar on your page

```
var all = document.getElementsByTagName("*"), i = 0, rect, docWidth = document.documentElement.offsetWidth;
for (; i < all.length; i++) {
    rect = all[i].getBoundingClientRect();
    if (rect.right > docWidth || rect.left < 0){
        console.log(all[i]);
        all[i].style.width = '200px';
    }
}
```

## Usage
    1 - Just copy & paste this code on the console after rolling the scrollbar to the right of your site.
    2 - You can change this line ".style.width = '200px'" if you wanna highlight it in a different way.

---

# Reference: [StackOverflow](https://stackoverflow.com/questions/31458477/find-element-that-is-causing-the-showing-of-horizontal-scrollbar-in-google-chrom)
