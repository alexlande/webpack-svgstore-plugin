```javascript

...
//load plugins
plugins: [
  //create svg sprite from /path/to/*.svg
  new SvgStore('/path/to/folder/svg', {
    prefix: 'icon-',
    svg: {
      style: 'position:absolute; width:0; height:0',
      xmlns: 'http://www.w3.org/2000/svg'
    },
    output: [
      // multiply sprites
      // - prefix
      {
        svg: 'Logo-',
        sprite: path.join(_path + '/public/assets/svg/_logo_sprite.html')
      },
      // - except prefix
      {
        svg: 'except-Logo-',
        sprite: path.join(_path + '/public/assets/svg/_sprite.html')
      }

      // 1 sprite
      {
        svg: 'all',
        sprite: path.join(_path + '/public/assets/svg/_sprite.html')
      }

    ],
    loop: 2,
    min: true
  })
]


```