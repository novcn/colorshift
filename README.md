# Usage

```bash
usage : colorshift [ options ] 

  options:
    -h | --help           show help
    --verbose             verbose logging
    -l | --limit          limit color output from wrapping around
    -r | --red <value>    modify red by <value>
    -g | --green <value>  modify green by <value>
    -b | --blue <value>   modify blue by <value>
    -a | --alpha <value>  modify alpha by <value>
```

# Examples

Simply add values to each color
``` bash
λ › colorshift -r de -g ad -b be -a ef '#0000000'
#DEADBEEF
```

Wrap around arithmetic by default
``` bash
λ › colorshift -r 1 '#FF000000'
#00000000
```

Limit option disables wrap-around 
``` bash
λ › colorshift -r 1 -l '#FF000000'
#FF000000
```

Subtraction supported too
``` bash
λ colorshift -r -1 '#FF000000'
#FE000000
```

Invert a color - this ignores the alpha value
``` bash
λ colorshift -v '#000000de'
#FFFFFFDE
```
