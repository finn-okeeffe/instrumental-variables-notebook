# Instrumental variables synthetic study
This notebook is an exploration of instrumental variables and two-stage least squares. This is a way to try and get at causal relationships when randomised control trials aren't feasible. This particular example looks at the causal association between years of education and wages, when both of these variables are affected by a confounder we call 'Motivation'.

## Synthetic data structure
```mermaid
dtc[Distance to college]
motivation[Motivation]
yoe[Years of education]
wages[Wages]
r((Residual))

dtc --> yoe
motivation --> yoe
yoe --> wages
motivation --> r --> wages
```

## Inspiration
This notebook is mostly following along with the YouTube video [Instrumental Variables in Action: Education and Wages (graphs): Causal Inference Bootcamp](https://www.youtube.com/watch?v=vacBsxBgFMY).
I also encourage you to check out Greg Hancock and Patrick Curran's podcast Quantitude, they have a great episode on this: [Instrumental Variables (Dad)Rock!](https://open.spotify.com/episode/3k8MXmocl478aj9Eud4sQx?si=fecf2beb20724b21).
