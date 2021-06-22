# ATDx Report Summary
Our ATDx analysis targets a portfolio of software projects and identifies the pain points of each project in terms of Architectural Technical Debt (ATD). This evaluation is based on a statistical analysis of the violations of SonarCloud rules.

## ATDx in a nutshell
![ATDx in a nutshell](https://raw.githubusercontent.com/S2-group/ATDx_reports/master/plots/atdx_in_a_nutshell.jpg)
ATDx works by comparing architectural debt metrics across the projects of a software portfolio. Intuitively, it ensures that measurements across different projects are comparable, and then evaluates the severity of Architectural Technical Debt by confronting the measurements across the projects.
The ATDx approach is by itself tool-independent, and can be customized according the analysis tools available, and the portfolio considered.
In the case of this report, we used an instance of ATDx based on the static analysis tool [SonarQube](https://www.sonarqube.org/).
The instance of ATDx used to analyze your projects provides an overview of the architectural technical debt in a project in 6 distinct dimensions:
* **Inheritance**: flaws concerning inheritance mechanisms between classes, such as overrides and inheritance of methods or fields
* **Exception**: flaws regarding the management of Java exceptions and the subclassing of the “Exception” Java class.
* **JVMS**: potential misuses of the Java Virtual Machine, e.g., the incorrect usage of the specific Java class “Serializable”
* **Threading**: flaws arising from the implementation of multiple execution threads, which could potentially lead to concurrency problems
* **Interface**: flaws related to the usage of Java interfaces
* **Complexity**: flaws derived from prominent complexity measures, such as McCabe’s cyclomatic complexity

For each project, the dimensions assume a value between 0 and 5, where 0 denotes minimum architectural debt of the project in that dimension, and 5 maximum architectural debt.
In the reminder of this report, we firstly provide a set of radar charts (one for each project). Then for each project we give:
1. The same radar chart as shown at the beginning
2. A table showing the top-10 classes of the project with the highest architectural technical debt.
Note that if numerous classes with 1 violation are reported, this might point to a widespread problem (only a maximum of 10 classes are provided per project for the sake of readability). Similarly, empty rows indicate that only a few classes are affected by ATDx violations.
If you are curious about more theoretical background on ATDx, you can have a look at [this scientific publication](https://robertoverdecchia.github.io/papers/ENASE_2020.pdf).

## ATDx radar charts of your projects
### Analysed project apache_sling-org-apache-sling-commons-html
The atdx for this project is: 0.05476078521745012

![Radarchart](https://github.com/Sebastian-Ospina/atdx_report/blob/main/reports/apache_sling-org-apache-sling-commons-html.jpg "Radarchart of your project")
<p style="text-align:left">[Project on Github](https://github.com/apache_sling-org-apache-sling-commons-html) <br> [Project on SonarCloud ](https://sonarcloud.io/dashboard?id=apache_sling-org-apache-sling-commons-html) <br></p>

# ATDx project report summaries
## Project apache_sling-org-apache-sling-commons-html_
<img src="https://github.com/Sebastian-Ospina/atdx_report/blob/main/reports/apache_sling-org-apache-sling-commons-html.jpg"/><p style="text-align:left">[Project on Github](https://github.com/apache_sling-org-apache-sling-commons-html) <br> [Project on SonarCloud ](https://sonarcloud.io/dashboard?id=apache_sling-org-apache-sling-commons-html) <br></p>

### Top classes with architectural debt violations
| Class name                 | Complexity   | Interface   | Exception   | Member   | Inheritance   | Vmsmell   | Naming   | Constants   | Threading   | Variables   | Lockin   | Project                                    |
|:---------------------------|:-------------|:------------|:------------|:---------|:--------------|:----------|:---------|:------------|:------------|:------------|:---------|:-------------------------------------------|
| TagParser.java             | 15           | 3           | 8           | 3        | 0             | 0         | 0        | 0           | 0           | 0           | 0        | apache_sling-org-apache-sling-commons-html |
| Token.java                 | 0            | 8           | 0           | 8        | 0             | 0         | 0        | 0           | 0           | 0           | 0        | apache_sling-org-apache-sling-commons-html |
| ParseException.java        | 0            | 3           | 4           | 3        | 0             | 0         | 0        | 0           | 0           | 0           | 0        | apache_sling-org-apache-sling-commons-html |
| SimpleCharStream.java      | 2            | 3           | 1           | 1        | 0             | 0         | 0        | 0           | 0           | 0           | 0        | apache_sling-org-apache-sling-commons-html |
| TagParserTokenManager.java | 0            | 1           | 1           | 4        | 0             | 0         | 0        | 0           | 0           | 0           | 0        | apache_sling-org-apache-sling-commons-html |
| -                          | -            | -           | -           | -        | -             | -         | -        | -           | -           | -           | -        | -                                          |
