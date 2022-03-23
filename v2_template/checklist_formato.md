# CHECKLIST DE FORMATO

CONSIDERACIONES GENERALES PARA TODO EL INFORME:
-	**Hoja Formato** A4
    OK: en main_doc.tex (\documentclass[oneside, 11pt]{book}) 

-	**Tipo de Letra**: Arial 11 o Times New Roman 11.
    OK: fuente Times-like (\usepackage{times} en formato_PI.sty)

-	Impresión preferentemente **doble faz**
    OK: twoside (\documentclass[a4paper, 11pt, twoside]{book} en main_doc.tex)

-	**Numeración de hojas**:
    - Para cuerpo de informe,  desde el Capítulo 1 en adelante: **Numeración arábiga** (1, 2 ..)
    - Desde la Portada hasta Capítulo 1: **numeración romana** (i, ii, iii, iv…) 
    - La portada *se cuenta* pero **no se numera**.

-	**Márgenes**: Superior e Inferior y derecho: 2,5 cm; izquierdo 3 cm
    OK: \usepackage[a4paper, left=3cm,right=2.5cm,top=2.5cm,head=2.5cm,bottom=2.5cm]{geometry} en formato_PI.sty

-	**Interlineado**: 
    - **Interlineado en el texto**: 1,5 espacios. 
    OK: \renewcommand{\baselinestretch}{1.5}  en formato_PI.sty 
    - **Notas y citas textuales**: espacio simple.
    OK: \setstretch{1}

            or
    
        \begingroup     
            \setstretch{1}                  
        \endgroup

        en el lugar donde se necesite interlineado simple.

-	Distribuir el contenido en:

    1. Capítulo 1  (negrita, tamaño 14)
        
    2. 1.1. Sección (negrita, tamaño 12)

    3. 	1.1.1 Sub-sección (normal, tamaño 12)
            
        SI = se sigue la numeracion recomendada (numeración arábiga)
        NO = se mantiene el tamaño y espaciado de titlos de cada parte del documento (Valores estándar en: [8.2 - Standard Classes - titlesec](https://ctan.dcc.uchile.cl/macros/latex/contrib/titlesec/titlesec.pdf))

        1. Capítulos: 
            - Título
                \titleformat{\chapter}[display]
                {\normalfont\huge\bfseries}{\chaptertitlename\ \thechapter}{20pt}{\Huge}
            - Espaciado de título
                \titlespacing*{\chapter} {0pt}{50pt}{40pt}
        2. Secciones:
            - Título 
                \titleformat{\section}
                {\normalfont\Large\bfseries}{\thesection}{1em}{}
            - Espaciado de título
                \titlespacing*{\section} {0pt}{3.5ex plus 1ex minus .2ex}{2.3ex plus .2ex}
        3. Subsecciones:
            - Título
                \titleformat{\subsection}
                {\normalfont\large\bfseries}{\thesubsection}{1em}{}
            - Espaciado de título
                \titlespacing*{\subsection} {0pt}{3.25ex plus 1ex minus .2ex}{1.5ex plus .2ex}


-   Redacción del texto (normal, tamaño 11)
    OK: fuente Times-like (\usepackage{times} en formato_PI.sty) Y \documentclass[oneside, 11pt]{book} en main_doc.tex 

-	Después del Título de Capítulo o Secciones: 3 espacios. 
    NO: Se mantienen valores por default de Latex. Ver en ítem anterior correspondiente

-	Las Imágenes y Tablas se separan del texto con 3 espacios.
    NO: se mantienen valores estandares de Latex. 

    The text float sep (\textfloatsep) is 20.0pt plus 2.0pt minus 4.0pt 
    The float float sep (\floatsep) is 12.0pt plus 2.0pt minus 2.0pt 
    The distance between text and floats inserted inside page text using h (\intextsep) is 12.0pt plus 2.0pt minus 2.0pt


-	En el apartado Bibliografía ÚNICAMENTE van los libros en papel o e-book que en general tienen ISBN.
    OK: \addbibresource{bibliografia.bib} en formato_PI.sty
        \printbibliography[type=book, title=Bibliografía] en main_doc.tex

-	En el apartado REFERENCIAS van todo lo que no son libros, como  links, apuntes, etc. 
    OK: \addbibresource{referencias.bib} en formato_PI.sty
        \printbibliography[nottype=book, title=Referencias] en main_doc.tex

-   Se numera corrido de ésta forma: [12], iniciando en Bibliografía y continuando la numeración en Referencias. 
    OK:
