# A Semi-Automated BPMN-based Framework for Detecting Conflicts between Security, Data-minimization and Fairness Requirements
Qusai Ramadan, Daniel Strüber, Mattia Salnitri, Jan Jürjens, Volker Riediger, Steffen Staab

In this file, we present the artifact used in our paper. Our submission includes
a prototypical implementation of our work on top of STS, the supporting
tool for the BPMN extension [SecBPMN2](http://www.secbpmn.disi.unitn.it/), whose security requirements
we reused. Our implementation supports the two main contributions of this work: First,
the modeling of security, data-minimization and fairness requirements in BPMN models, using
a suitable model editor. Second, formulating security, data-minimization and fairness requirments as SecBPMN2-Q queries 
that can be verified against security-, data-minimization- and fairness-annotated BPMN model for alignment verification purpose.
Third, automated conflict analysis in data-minimization-, security-, and fairness-annotated BPMN models, 
based on our catalog of anti-patterns.

# Resources

* **Artifact: a healthcare case study and a catalog of domain-independent anti-patterns:** https://figshare.com/s/a9917ca83c1a07b88d56
* **Artifact: Mirrors of the STS-tool current versions:** http://www.sts-tool.eu/downloads/secbpmn-dm/
* **The Experimental Evaluation Artifacts: for transparency we share all our experimental materials:** https://figshare.com/s/29c1deea98af68882c78

## Performing automatic conflicts detection. 
To view and analyze our designed models please follow the instructions:
* Install the STS tools from [here](http://www.sts-tool.eu/downloads/secbpmn-dm/) .
* Download the *telemedicine.exp* file from [here](https://figshare.com/s/a9917ca83c1a07b88d56) to your desktop. This file is automatically generated from the STS tool and it contains all the SecBPMN2 models of our case study.

* To view and modify the models in this file you need to import it into the STS:
 * In the STS tool, do *File→ Import → project → next → select the "telemedicine.exp" file from your desktop*. 
 * The projects contains two SecBPMN2 models namely, "SoSyM19-PaperExample.bpmnl" and Full_annotatedModel.bpmnl". 
 * The project contains a catalog of domain-independent anti-patterns.
 * To run a conflict analysis open the SecBPMN2 model you want to analyse from the following directory: */SoSym19-telemedicine/Models/SecBPMN2/Business process/*
 * In the STS tool, do *Analysis→ Check Security Policy*. 
 * The conflicts analysis will take few minitues. Once the analysis is finish press *OK*
 * The analysis result will be shown as texuall messages in new window. The messages will be of two types "Error" or "Warning". The former represnts conflict while the later represent potential conflict.
 * To view the anti-patterns find the following dirctory */SoSyM19-telemedicine/Models/SecBPMN2/Conflicts_Patterns*
