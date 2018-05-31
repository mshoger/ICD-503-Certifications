# FedRAMP-Certifications
GSA Specific Certifications for [Compliance Masonry](https://github.com/opencontrol/compliance-masonry)

To import these data into a OpenControl project add the follow code to your opencontrol.yaml file.
```yaml
dependencies:
  certifications:
    - url: https://github.com/opencontrol/FedRAMP-Certifications
      revision: master
```

Once imported into your OpenControl content, [Compliance Masonry](https://github.com/opencontrol/compliance-masonry) and [FedRAMP Templater](https://github.com/opencontrol/fedramp-templater) can be used to generate template System Security Plans (SSPs):
```
compliance-masonry get
compliance-masonry docs gitbook FedRAMP-high
fedramp-templater fill opencontrols/ ./path_to_fedramp_templates/FedRAMP-System-Security-Plan-Template-v2.1.docx exports/FedRAMP-filled.docx
```

For more information on the opencontrol.yaml visit the [Compliance Masonry CLI](https://github.com/opencontrol/compliance-masonry#creating-an-opencontrol-project).
