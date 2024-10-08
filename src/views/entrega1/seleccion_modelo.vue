<template>
  <div class="container">
    <div class="header">
      <h1>Entrega 1: Selección del Modelo</h1>
    </div>
    <div class="content">
      <p>
        La propuesta de proyecto final para Minería de Datos en la Maestría de Ingeniería de Sistemas consiste en utilizar una fuente de créditos activos
        suministrada por Datos Abiertos para determinar, con base al perfil de las personas, los beneficios crediticios a los que podrían acceder.
      </p>
      <h3>Modelo Escogido: <a href="https://en.wikipedia.org/wiki/Gradient_boosting" target="_blank">Gradient Boosting Machine (GBM)</a></h3>
      <h3>Justificación:</h3>
      <p>
        Los modelos GBM (Gradient Boosting Machines) son muy efectivos para manejar información estructurada tabularmente, 
        la cual es la estructura comúnmente manejada para almacenar datos financieros. Además, tiene la capacidad de trabajar 
        con un gran número de datos categóricos y numéricos [1], lo cual es perfecto para un caso de perfilamiento como el de este proyecto, 
        donde se deben tener en cuenta descripciones de las personas. Funcionalmente, este modelo realiza un conjunto de árboles de decisión 
        donde los árboles sucesivos intentar corregir los errores previos. Si bien este modelo posee una alta precisión, 
        resistencia al sobreajuste y capacidad de capturar relaciones no lineales, para lograrlo conlleva un alto costo computacional. 
        No obstante, se podría argumentar que estas ventajas superan los costos. Así mismom hay GBMs más ligeras para un procesamiento 
        más rápido y menos exigente.
      </p>
      <h3>Relevancia:</h3>
      <p>
        Las GBM son actualmente utilizadas en la industria financiera para calificación crediticia, detección de fraudes y evaluación de riesgos. 
        Al poder manejar datos grandes, complejos y con múltiples características, son adecuadas para predecir beneficios crediticios con base al 
        perfil de las personas. Estudios han demostrado que GBM supera a otros modelos de aprendizaje automático (incluyendo los de aprendizaje 
        profundo) en diversas aplicaciones financieras, debido a su eficiencia y menor demanda computacional para niveles de precisión similares [2]. 
        Además, gracias a su composición, es capaz de manejar datos desequilibrados, lo cual es común en entornos financieros.
      </p>
      <h3>Librerías:</h3>
      <ul>
        <li><a href="https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html" target="_blank">Scikit-learn:</a> Es una librería de aprendizaje automático que incluye una implementación de GBM.</li>
        <li><a href="https://xgboost.readthedocs.io/en/stable/" target="_blank">XGBoost:</a> Es una implementación eficiente y escalable de GBM.</li>
        <li><a href="https://lightgbm.readthedocs.io/en/stable/" target="_blank">LightGBM:</a> Es una versión ligera y más rápida para implementar GBM.</li>
        <li><a href="https://catboost.ai/" target="_blank">CatBoost:</a> Es una librería de GMB especializada para variables categoricas.</li>
      </ul>
      <h3>Referencias:</h3>
      <ol>
        <li>
          M. Reyners, "An Introduction to Gradient Boosting," Winter School on Quantitative Finance, Univ. of Amsterdam, 2019
          Disponible: <a href=https://staff.fnwi.uva.nl/p.j.c.spreij/winterschool/19ReynersPaper.pdf>https://staff.fnwi.uva.nl/p.j.c.spreij/winterschool/19ReynersPaper.pdf</a>. [Accedido: 18-ago-2024].
        </li>
        <li>
          M. Schmitt, "Deep Learning vs. Gradient Boosting: Benchmarking state-of-the-art machine learning algorithms for credit scoring,"
          arXiv, May 2022. Disponible: <a href=https://arxiv.org/abs/2205.10535>https://arxiv.org/abs/2205.10535</a>. [Accedido: 18-ago-2024].
        </li>
        <li>
          Dataset fuente: 
          "Tarjetas de crédito Colombia," Datos Abiertos Colombia, 
          <a href="https://www.datos.gov.co/Econom-a-y-Finanzas/Tarjetas-de-cr-dito-Colombia/innv-fdhy">https://www.datos.gov.co/Econom-a-y-Finanzas/Tarjetas-de-cr-dito-Colombia/innv-fdhy</a>.
          [Accedido: 18-ago-2024].
        </li>
      </ol>
    </div>
    <div class="footer">
        Fecha de Entrega: Agosto 18, 2024
        <br>
        Desarrollado por: Giuliano Frieri
    </div>
  </div>
</template>

<script>
export default {
  name: 'seleccion_modelo',
};
</script>

<style scoped>
/* Estilo minimalista para la página */
.container {
  background-color: #ffffff;
  border-radius: 12px;
  padding: 20px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
}

.header h1 {
  font-size: 28px;
  color: #333;
}

.content p {
  font-size: 16px;
  line-height: 1.6;
  color: #555;
}

.content h3 {
  color: #444;
  margin-top: 20px;
}

.content a {
  color: #007bff;
  text-decoration: none;
}

.content a:hover {
  text-decoration: underline;
}

ul {
  list-style: none;
  padding: 0;
}

ul li {
  margin-bottom: 10px;
}

.footer {
  text-align: right;
  font-size: 14px;
  color: #777;
  margin-top: 30px;
}
</style>
