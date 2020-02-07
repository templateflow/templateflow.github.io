---
layout: default
---

Group inference and reporting of neuroimaging studies require that individual's features are spatially aligned into a common frame where their location can be called standard ([Brett et al., 2002][1]).
To that end, a multiplicity of brain templates with anatomical annotations (i.e. atlases) have been published ([Dickie et al., 2017][2]).
However, a centralized resource that allows programmatic access to templates is lacking.
_TemplateFlow_ is a modular, version-controlled resource that allows researchers to use templates "off-the-shelf" and share new ones.

# Components

  * **Repository of templates**: We use [DataLad][3] to maintain the templates under version control ([repository][4])
  * **Python client**: An easy to use query tool ([link to documentation][5]):

    ```Python
    >>> from templateflow import api as tflow
    >>> tflow.get('MNI152NLin6Asym', desc=None, resolution=1, suffix='T1w', extension='nii.gz')
    PosixPath('/home/oesteban/.cache/templateflow/tpl-MNI152NLin6Asym/tpl-MNI152NLin6Asym_res-01_T1w.nii.gz')
    ```

![Branching](assets/poster-templateflow.png) 

[1]: https://doi.org/10.1038/nrn756 "The problem of functional localization in the human brain."
[2]: https://dx.doi.org/10.3389%2Ffninf.2017.00001 "Whole Brain Magnetic Resonance Image Atlases: A Systematic Review of Existing Atlases and Caveats for Use in Population Imaging"
[3]: https://datalad.org "DataLad"
[4]: https://github.com/templateflow/templateflow "TemplateFlow repository"
[5]: https://templateflow.github.io/python-client "TemplateFlow Python client documentation"
