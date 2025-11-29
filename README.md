<img src="MOFCreatioNN.jpg" width="500" />

<H1>MOFCreatioNN</H1>

<H2>Table of Contents</H2>
<ul>
  <li><a href="#introduction">Introduction</a></li>
  <li><a href="#features">Features</a></li>
  <li><a href="#repository-structure">Repository Structure</a></li>
  <li><a href="#trained-models">Trained Models</a></li>
  <li><a href="#datasets">Datasets</a></li>
  <li><a href="#usage">Usage</a></li>
  <li><a href="#contributing">Contributing</a></li>
  <li><a href="#license">License</a></li>
</ul>

<H2 id="introduction">Introduction</H2>
<p>
MOFCreatioNN is an integrated computational framework for the design, evaluation, 
and cost estimation of Metal–Organic Frameworks (MOFs). The system incorporates:
</p>

<ul>
  <li>Reinforcement-learning MOF generation</li>
  <li>Crystal Graph Convolutional Neural Networks (CGCNNs)</li>
  <li>A multi-stage prediction funnel for stability, catalytic ability, cost, sustainability, and adsorption</li>
  <li>Automated XRD simulation, property prediction, and fitness scoring</li>
</ul>

<p>
This framework enables large-scale screening of both experimental MOFs and AI-generated MOFs 
for catalytic, adsorption, and economic applications. 
</p>

<H2 id="features">Features</H2>
<ul>
  <li><b>Cost Estimation Dataset:</b> A curated dataset assigning industrial cost values to each element in its commonly used form.</li>
  <li><b>Trained CGCNN Modules:</b> Pre-trained neural network models for predicting MOF properties including stability, adsorption, selectivity, cost, and synthesis likelihood.</li>
  <li><b>Reinforcement-Learning MOF Generator:</b> Constructs chemically valid MOFs using tokenized metal clusters and linker fragments.</li>
  <li><b>Multi-Stage Prediction Funnel:</b> Efficient filtering using quantile-based thresholds, significantly reducing computational cost while preserving top-performing candidates.</li>
  <li><b>Full Reproducibility:</b> All scripts, datasets, models, and preprocessing tools required to reproduce results in the associated publication.</li>
</ul>

<H2 id="repository-structure">Repository Structure</H2>
<p>GitHub Repository: 
<a href="https://github.com/SatyaK-0/MatCreatioNN/tree/main">
https://github.com/SatyaK-0/MatCreatioNN/tree/main
</a></p>

<ol>
  <li>
    <b>MachineLearningPredictionModels_PTHFiles/</b> –
    Contains the trained PyTorch <code>.pth</code> model files for all 13 CGCNN predictors 
    used in the funnel/filtration system.
  </li>

  <li>
    <b>LogicProof/</b> –
    A script demonstrating that the ordering of funnel stages does not affect 
    final outcomes when using quantile-based filtering.
  </li>

  <li>
    <b>SupportingPythonPrograms_Implementation_DataProcessing/</b> –
    Supporting scripts for:
    <ul>
      <li>Reinforcement-learning MOF generation</li>
      <li>PyMatGen-based XRD simulation</li>
      <li>Molecular cost calculator</li>
      <li>Post-processing of funnel outputs</li>
      <li>Normalization, visualization, and utility functions</li>
    </ul>
  </li>

  <li>
    <b>cgcnn/</b> –
    Modified and bug-fixed CGCNN implementation updated for compatibility 
    with modern PyTorch and Python versions.
  </li>
</ol>

<H2 id="trained-models">Trained Models</H2>
<p>
This repository contains pre-trained neural-network models for all MOF-related predictions 
performed in the MOFCreatioNN framework, including:
</p>

<ul>
  <li>Thermal and water stability predictors</li>
  <li>CO₂ adsorption and CO₂/H₂O selectivity models</li>
  <li>Available surface area predictor</li>
  <li>Synthesis likelihood classifier</li>
  <li>Elemental cost and sustainability regressors</li>
</ul>


<H2 id="usage">Usage</H2>
<p>
To run the full pipeline:
</p>

<ol>
  <li>Install Python ≥ 3.10 and PyTorch ≥ 2.0.</li>
  <li>Clone the repository and install required dependencies.</li>
  <li>Use the provided scripts in 
      <code>SupportingPythonPrograms_Implementation_DataProcessing/</code> 
      to generate structures, compute descriptors, and evaluate funnel performance.
  </li>
</ol>

<p>
Each directory contains additional documentation or comments to guide usage.
</p>

<H2 id="contributing">Contributing</H2>
<p>
Contributions are welcome! To contribute:
</p>

<ol>
  <li>Fork the repository.</li>
  <li>Create a new branch for your feature or fix.</li>
  <li>Commit your changes and push the branch.</li>
  <li>Open a pull request with a clear explanation of your contribution.</li>
</ol>

<H2 id="license">License</H2>
<p>
This project is released under the MIT License unless otherwise specified.
</p>

