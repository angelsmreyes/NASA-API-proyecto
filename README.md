# NASA-API

![image.png](attachment:image.png)

Este proyecto tuvo como finalidad el extraer datos usando la [API](https://api.nasa.gov) de la NASA.

De allí se utilizo la base de datos de exoplanetas, de la cual se utilizo la tabla de exoplanetas detectados con la tecnica de microlensing con una 
dimensión de  y la tabla de Planetary Systems Composite que contiene todos los exoplanetas detectados por diferentes tecnicas.

De la tabla microlensing se seleccionaron los siguientes atributos: 

- **pl_name:** Planet Name (Planet name)
- **rastr:** RA (Right ascension of the microlensing event, in sexagesimal format
- **decstr:** Declination of the microlensing event, in sexagesimal format
- **pl_masse:** Mass of planet, in Earth masses
- **pl_massj:** Planet Mass (Mass of planet, in Jupiter masses)
- **pl_orbsmax** Planet-star Projected Semi-major Axis, unidad = Astronomical unit (au) 
- **sy_dist:** Lens Distance, unit = Parsec (pc)
- **ml_dists:** Source Distance, unit = Parsec (pc)
- **ml_xtimeein:** Einstein Crossing Time, unit=days 
- **ml_massratio:** Planet-star Mass Ratio (10^-4)
- **ml_magis:** Source I-band unit = mag 
- **ml_radeinang:** Angular Einstein Radius, unit = mas 

Se puede visitar la siguiente [documentación](https://exoplanetarchive.ipac.caltech.edu/docs/microlensing-column-mapping.pdf) para una explicación de el significado de cada una de las columnas y lo que representa:

Se aplicaron metodos de data cleaning y data wrangling en ambos dataframes. Luego se combino un subset de planetas de microlensing de Planetary System Composite y se hizo un merge con la tabla de microlesing con la finalidad de obtener 
valores para las columnas de la masa del planeta comparada con la masa de la tierra y de jupiter. 

Obteniendo un total de tres dataframes (microlensing, plaetary composite systems and y el merge).