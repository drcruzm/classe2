# Clase 2 Intro Dataframe

## Instalando la librería
    # install.packages("UsingR")
    # install.packages("DataExplorer")
## Llamado de Librerías
    library(lattice)
    library(survival)
    library(Formula)
    library(ggplot2)
    library(MASS) 
    library(HistData)
    library(Hmisc)
    library(UsingR)
    library(DataExplorer)
## Leyendo los datos
    data("nym.2002")
    head(nym.2002)
          place gender age home     time
    3475   3592   Male  52  GBR 217.4833
    13594 13853 Female  40   NY 272.5500
    12012 12256   Male  31  FRA 265.2833
    10236 10457 Female  33   MI 256.1500
    9476   9686   Male  33   NY 252.2500
    1720   1784   Male  40   NJ 201.9667
## Estadística Descriptiva
    mean(nym.2002$age)
    [1] 39.1
    hist(nym.2002)
![](https://paper-attachments.dropbox.com/s_79429FB258D6F40E0AE9A0A9CB24C1933653DA4C857905146E1EA0926F5110CC_1629261528037_unnamed-chunk-4-1.png)

## Customizando el Histograma
    hist(nym.2002$age, col="lightblue", main = "Edades Maraton", xlab = "Edades", freq = TRUE, labels = TRUE)
    abline(v= mean(nym.2002$age), col='red')
![](https://paper-attachments.dropbox.com/s_79429FB258D6F40E0AE9A0A9CB24C1933653DA4C857905146E1EA0926F5110CC_1629261546011_unnamed-chunk-5-1.png)

## Liberia Data Explorer

**Reporte**

    # create_report(nym.2002)
## Grafica de Barras
    plot_bar(nym.2002)
    1 columns ignored with more than 50 categories.
    home: 73 categories
![](https://paper-attachments.dropbox.com/s_79429FB258D6F40E0AE9A0A9CB24C1933653DA4C857905146E1EA0926F5110CC_1629261421685_Data+Explorer+2-1.png)

## Histogramas
    plot_histogram(nym.2002)
![](https://paper-attachments.dropbox.com/s_79429FB258D6F40E0AE9A0A9CB24C1933653DA4C857905146E1EA0926F5110CC_1629261433234_Data+Explorer+3-1.png)

    plot_histogram(nym.2002$time)
![](https://paper-attachments.dropbox.com/s_79429FB258D6F40E0AE9A0A9CB24C1933653DA4C857905146E1EA0926F5110CC_1629261444121_Data+Explorer+4-1.png)

## Grafica de Densidad
    plot_density(nym.2002)
![](https://paper-attachments.dropbox.com/s_79429FB258D6F40E0AE9A0A9CB24C1933653DA4C857905146E1EA0926F5110CC_1629261453609_Data+Explorer+5-1.png)

## Box plot
    plot_boxplot(nym.2002, by = "age")
![](https://paper-attachments.dropbox.com/s_79429FB258D6F40E0AE9A0A9CB24C1933653DA4C857905146E1EA0926F5110CC_1629261464971_Data+Explorer+6-1.png)

    plot_boxplot(nym.2002, by = "time")
![](https://paper-attachments.dropbox.com/s_79429FB258D6F40E0AE9A0A9CB24C1933653DA4C857905146E1EA0926F5110CC_1629261476197_Data+Explorer+7-1.png)


