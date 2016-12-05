
## Impressions Potential vs Adimark

#### Objetivo
Cear una herramienta de medición del impacto en Twitter de cada candidato presidencial, bajo el contexto que su presencia en dicha red social determina lo que piensa un conjunto relevante del electorado en Chile, y se traduciría en una muestra real de sus aspiraciones a transformarse en el o la presidenta de Chile.

#### Método
1. Se ecogen precandidatos(as) presidenciales de acuerdo al último listado de precandidatos que entregó en Noviembre la encuesta Adimark.

2. Se desarrolla una herramienta en el entorno programación node.js/npm para la recolección de las métricas correspondientes a los últimos tweets realizados por cada candidato. En este caso, con fines de demostrar la potencialidad de la herramienta, se utiliza solamente el último tweet de cada precandidato.

3. Se utiliza la definición operativa de *potential impressions (PI)* para determinar el impacto de los tweets de los candidatos, independiente de su contenido: "Número total de veces que un tweet aparece en el timeline de otro usuario" ([Kevin Shively](http://simplymeasured.com/blog/potential-impressions-vs-actual-impressions-which-should-you-measure/#sm.01ibb7q419o4ei111h81jlsjcytjm), 2015)

4. Fórmula para el cálculo de *Potential impressions*:

|Author|Tweet|Followers(F)|PI|Notes|
|:---|:---|:---|:---|:---|
|decort|@some message|8000|1600|20% F|
|schoeny|No @some message|5000|5000|F|
|aviel|some message|2000|2000|F|
Fuente: Kevin Shively, 2015.

#### Resultados
Aplicada la fórmula solamente para el último tweet de cada candidato presidencial, se obtuvo lo siguiente:

|Candidato|Impressions Potential|Adimark|
|:---|:---|:---|
|Sebastian Piñera|58.2|24|
|Marco Enríquez-Ominami|19.1|	1|
|Felipe Kast|	7.5|	1|
|Ricardo Lagos E.	|5.2|	7|
|Carolina Goic	|4.3	|1|
|Manuel José Ossandón	|3.6|	4|
|Alejandro Guillier	|2.0	|21|
|José Miguel Insulza	|0.2|	1|

- Se observa que Piñera aventaja a los demás candidatos con un amplio porcentaje, incluso a Guillier, quien en Twitter parece tener menor impacto.
- El caso opuesto es MEO, quien se posiciona como la segunda preferencia en Twitter, pero presenta con un escaso porcentaje en Adimark.
- El resto de los candidatos presenta cifras similares entre sus porcentajes de PI y lo que reporta Adimark. Solamente Felipe Kast y Carolina Goic presentan un porcentaje significativamente más alto en Twitter que en Adimar.

En la gráfica se puede apreciar de mejor forma:

<div>
    <a href="https://plot.ly/~crishernandezmaps/2/" target="_blank" title="" style="display: block; text-align: center;"><img src="https://plot.ly/~crishernandezmaps/2.png" alt="" style="max-width: 100%;width: 600px;"  width="600" onerror="this.onerror=null;this.src='https://plot.ly/404.png';" /></a>
    <script data-plotly="crishernandezmaps:2"  src="https://plot.ly/embed.js" async></script>
</div>

![](https://plot.ly/~crishernandezmaps/2/)
<iframe width="900" height="800" frameborder="0" scrolling="no" src="https://plot.ly/~crishernandezmaps/2.embed"></iframe>

- Si tomamos ambos índices y se visualizan como una coordenada en la que Twitter sopesa el valor entregado por Adimark, se aprecia que Piñera y Guillier se alejan del resto de los candidatos. Guillier sin embargo, al parecer posee mayor impacto en la prensa y televisión, más que en Twitter.

#### Alcances
Este ejercicio 'básico' representa solamente una muestra de lo que se puede lograr creando mayores filtros que resuelvan el sesgo de la medición en Twitter. Se consideran dos pasos adicionales para resolver dicho sesgo:

1. Medir el impacto de los mensajes de cada candidato aplicando lo propuesto en términos del *Indegree influence*, *Retweet influence* y *Mention influence* (Cha, Haddadi,Benevenuto,Gummadi. 2010). Definidas como:

  - **Indegree influence**, the number of followers of a user, directly indicates the size of the audience for that user.
  - **Retweet influence**, which we measure through the number of retweets containing one’s name, indicates the ability of that user to generate content with pass-along value.
  - **Mention influence**, which we measure through the number of mentions containing one’s name, indicates the ability of that user to engage others in a conversation.

2. Reducir el sesgo por bots aplicando la herramienta desarrollada por Ferrara, Varol, Davis, Menczer y Flammini (2014): http://truthy.indiana.edu/botornot/

---
#### Sobre el autor de éste documento
Cristian Hernández es geógrafo de la Universidad de Chile, actualmente se encuentra trabajando en Londres dedicado a la ciencia de datos, es decir, al trabajo de la información y el rescate de ésta a través de análisis, visualización y programación de herramientas utilizando datos. Específicamente, trabaja en Common Action Forum. Fundación internacional con sede en Madrid dedicada a reunir a líderes en ámbitos como la política, la sociedad civil y la cultura para el desarrollo de soluciones globales que empoderen a los ciudadanos.

- Mail: crishernandez@gmail.com
- Twitter: @crishernandezco
- Web: http://crishernandez.co
