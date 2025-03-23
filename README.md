<h1>Obserbavles of spherical cpompact stars stars</h1>


_Adriel E. Rodríguez Concepción_

Facultad de Física, Universidad de La Habana, Cuba.
Instituto de Cibernética, Matemática y Física (ICIMAF), La Habana, Cuba.

<i>Este programa está diseñado para calcular todos los observables que sé calcularles a estrellas no magnetizadas, estáticas y estacionarias compuestas por un fluido isotrópico autogravitante. Calcula masa, radio, momento de inercia, segundo número de Love $$k_2$$, el parámetro adimensional de deformación de mareas $$\Lambda$$, el corrimiento al rojo gravitacional de las ondas electromagnéticas emitidas en la superficie, y la masa bariónica. El programa recibe una tabla con la ecuación de estado (barotrópica) y devuelve una tabla con los observables de  toda una secuencia de estrellas con dicha densidad central.</i>

<h2>Tidal Deformability</h2>

**Definición Newtoniana**

Supongamos que sobre un cuerpo esférico actúa un campo externo cuyo potencia se puede expandir en serie de potencias de la forma cuadrupolar:
    
    
$$U_{ext} = \dfrac{\epsilon}{3} P_l(\cos\theta) r^2$$

Sobre el cuerpo se inducirá un momento cuadrupolar $Q$ de forma que el potencial gravitatorio será:

$$ U(r,\theta) = - \dfrac{M}{r} - \dfrac{Q}{r^3} P_l(\cos\theta) + o(r^{-3}) + \dfrac{\epsilon}{3}r^2 P_l(\cos\theta) + o(r^3)$$

Considerando el caso de deformaciónes pequeñas, la respuesta será lineal de la forma $Q = -\lambda \epsilon$, siendo $\lambda$ el **parámetro de deformación de mareas**. Entonces el **segundo número de Love** se define por:
    
$$k_2= \dfrac{3}{2} \lambda R^{-5}$$

donde $R$ es el radio de la estrella.


Para calcularlo en la Teoría General de la Relatividad se siguen los siguientes pasos:
<ol>
    <li> Se escoge una métrica de <i>background</i> que será perturbada (en este caso será la esférica).
    <li> Se aplica una perturbación sobre la misma.
    <li> Se aplica una perturbación sobre el tensor de energía momentum del sistema.
    <li> Se obtien las ecuaciones de estructura para la métrica y el tensor de energía-momentum sin perturbar.
    <li> Se linearizan las ecuaciones de Einstein y se buscan las "ecuaciones de estructura" para las perturbaciones. Estas serán acopladas a las ecuaciones de estructura originales. 
    <li> Se resuleve el sistema. Aquí se obtienen los observables.
    <li> De la expansión en serie del coeficiente temporal para $r >> R$ se obtienen la relación $Q/\epsilon$ y, de esta, $k_2$.
</ol>


Tomaremos una métrica original de la forma :

$$ ds^2 = e^{\nu(r)}dt^2 - e^{\lambda(r)}dr^2 - r^2(d\theta^2 + \sin^2\theta d\phi^2),$$

con tensor de energía momentum (fluido perfecto) :

$$ T^\mu_\nu = \text{diag} [ \epsilon(r),- P(r),- P(r), -P(r) ].$$

A partir de las ecuaciones de Einstein

$$G^\mu_\nu = 8\pi  T^\mu_\nu$$

se obtienen la ecuaciones de estructura de Tolman-Oppenheimer-Volcoff.

$$e^\lambda = \left( 1- \dfrac{2 M(r)}{r} \right)^{-1}$$

$$M'(r) = 4\pi r^2 \epsilon(r)$$

$$\nu'(r) = \dfrac{2  (M(r) + 4 \pi r^3 P(r) )}{r (r - 2  M(r))} $$

$$P'(r) = - \dfrac{1}{2} (P(r) + \epsilon(r)) \nu'(r)$$


Ahora asumimos una perturbación sobre la métrica con la forma:

$$h_{\mu\nu} = \text{diag} [ e^{\nu(r)} H_0(r), - e^{\lambda(r)} H_2(r), -k(r) r^2,-k(r) r^2\sin^2\theta] P_l(\cos\theta)$$.

Las funciones de la perturbación $H_0,H_2,k$ se desprecian donde aparecen en orden mayor que 1.

Tomamos una perturbación sobre el tensor de energía-momentum de la forma:

$$ \delta T^\mu_\nu = \text{diag} [\delta \epsilon(r,\theta),-\delta P(r,\theta),- \delta P(r,\theta), -\delta P(r,\theta) ]$$

y se utiliza en las ecuaciones de Einstein lenearizadas, obteniéndose:

$$H_2 = - H_0$$

$$k' = - H_0' - H_0 \nu'$$

$$\delta P(r,\theta ) =  -\dfrac{ H_0(r) e^{-\lambda (r)} \left(\lambda '(r)+\nu '(r)\right)}{16 \pi  G r}P_l(\cos\theta)$$

$$\delta\epsilon(r,\theta) = \epsilon'(P(r))\delta P(r,\theta )$$ 

$$H_0''(r)+H_0'(r) \left(\frac{1}{2} \left(\nu '(r)-\lambda '(r)\right)+\frac{2}{r}\right)+H_0(r) \left(\frac{\epsilon '(P(r)) \left(\lambda '(r)+\nu '(r)\right)}{2 r}-\frac{6 e^{\lambda (r)}}{r^2}-\frac{1}{2} \lambda '(r) \nu '(r)+\frac{3 \lambda '(r)}{2 r}+\nu ''(r)-\frac{1}{2} \nu '(r)^2+\frac{7 \nu '(r)}{2 r}\right) = 0$$

La ecuación importante es la de $H_0$ puesto que esta función es la que aparece en el potencial gravitatorio y es la que se usará en el cálculo de $k_2$.

Para el vacío obtenemos:

$$h''(r)+h'(r) \left(\frac{2}{r}-\lambda '(r)\right)-h(r) \left(\frac{6 e^{\lambda (r)}}{r^2}+\lambda '(r)^2\right)= 0$$

siendo $h = {H_0}^{vacío}$.

Su solución es 
$$h(r) = c_1 {Q^2}_2\left(\frac{r}{M}-1\right) + c_2 {P^2}_2\left(\frac{r}{M}-1\right),$$

donde 

$$ {Q^2}_2(x) = \frac{-3 x^3+\frac{1}{2} \left(3 x^4-6 x^2+3\right) \log \left(\frac{x+1}{x-1}\right)+5 x}{x^2-1}$$

$$ {P^2}_2(x) = 3 \dfrac{ (1 - x)^2 (1 + x)}{-1 + x}$$

son las funciones asociadas de Legendre con $l=m=2$.

De la expansión se obtiene el potencial gravitatorio:

$$U(r,\theta) = - \dfrac{GM}{r} - \dfrac{4 c_1}{5}\left( \dfrac{GM}{r}\right)^3 P_2(\cos\theta) + \dfrac{3}{2}c_2 \left( \dfrac{r}{GM}\right)^2 P_2(\cos\theta)+ \ldots$$


De aquí se identifican las magnitudes:

$$Q = - \dfrac{4}{5}c1 (G M)^3$$

$$\epsilon = \dfrac{9}{2} c_2 (GM)^{-2}$$

$$\lambda =  \dfrac{8 c1 G^5 M^5}{45 c2}$$

$$k_2 = \dfrac{4 c1 G^5 M^5}{15 c2 R^5} =  \dfrac{4 c1 c^5}{15 c2 } $$

donde $c = \dfrac{M}{R}$ es la compacidad. La relación $c_1/c_2$ y la compacidad se obtienen de resolver las ecuaciones de estructura y la de $H_0$ acopladas dentro de la estrella. 

En lugar de $H_0$ en el interior se utiliza la función

$$y(r) = r\dfrac{H'(r)}{H(r)}$$

a partir de cuyo valor en la superficie de la estrella $yR$ y de la compacidad se obtiene la relación entre las constantes y el número de Love:


$$ k_2 = \frac{8 (1-2 c)^2 c^5 (2 c (\text{yR}-1)-\text{yR}+2)}{5 \left(2 c (c (2 c (c (2 c (\text{yR}+1)+3 \text{yR}-2)-11 \text{yR}+13)+3 (5 \text{yR}-8))-3 \text{yR}+6)-3 (1-2 c)^2 (2 c (\text{yR}-1)-\text{yR}+2) \log \left(\frac{1}{1-2 c}\right)\right)}$$

$$\Lambda = \frac{16 (1-2 c)^2 (2 c (\text{yR}-1)-\text{yR}+2)}{30 c (c (2 c (c (2 c (\text{yR}+1)+3 \text{yR}-2)-11 \text{yR}+13)+3 (5 \text{yR}-8))-3 \text{yR}+6)-45 (1-2 c)^2 (2 c (\text{yR}-1)-\text{yR}+2) \log \left(\frac{1}{1-2 c}\right)}$$

Para hallar $$y_R$$ resolvemos la ecuación de $$ y(r) = r\dfrac{H_0'(r)}{H_0(r)}$$ en el interior de la estrellas, que toma la forma:

$$r y'(r) + y^2(r) + F(r) y(r) + r^2 Q(r) = 0,$$


donde 

$$F(r) = \frac{1-4 \pi  G r^2 (\epsilon (r)-P(r))}{1-\frac{2 G M(r)}{r}},$$

$$Q(r) = \frac{4 \pi  G}{1-\frac{2 G M(r)}{r}} \left(\left((P(r)+\epsilon (r)) \epsilon '(P(r))+9 P(r)+5 \epsilon (r)\right)-\frac{6}{4 \pi  G r^2}\right)-\frac{4 G^2 \left(M(r)+4 \pi  r^3 P(r)\right)^2}{r^2 (r-2 G M(r))^2}$$

y como condición inical en el centro se usa $$y(0) = 2$$ que se obtiene de expandir en serie la ecuación diferencial de $$y$$ en el centro.

**Importante: ¡$$y_R$$ no siempre equivale a $$y(R)$$!**. Si se utiliza materia de quarks u otra ecuación de estado en la que la densidad de energía es distinta de cero en la superficie, o sea $$E_{surf} = E(P = 0) \ne 0 $$ entonces $$y_R = y(R) - \dfrac{4 \pi R^3}{M} E_{surf}$$ donde $$R$$ es el radio de la estrella y $$M$$ es su masa.

<h2>Moment of inercia</h2>
