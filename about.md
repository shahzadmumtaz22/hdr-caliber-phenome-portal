---
layout: home
title: About the HDR UK Phenotype Portal
---

## About

Welcome to HDR UK National Phenomics Resource Project, a project funded by [Health Data Research UK](https://www.hdruk.ac.uk).

When patients interact with physicians, or are admitted into hospital, information is collected electronically on their symptoms, diagnoses, laboratory test results, and prescriptions. This information is stored securely in Electronic Health Records (EHR) and is a valuable resource for researchers and clinicians for improving health and healthcare. EHRs are however of variable detail and quality and contain many inconsistencies. As a result, researchers and data providers spend considerable time creating complex computer programs to fix and statistically analyse the information in EHR and identify which patients have which disease. Currently, there is no means to share these tools across institutions in the UK resulting in duplication of effort. Reproducibility of research is also hampered as others do not have access to the precise methods and definitions used in a particular study. This project addresses these issues by creating an open resource for EHR users (researchers, clinicians, the NHS and data providers) to share their methods.

### What is ‘phenomics’?

Phenomics refers to the science of deriving new knowledge for health by studying multiple conditions in new ways. This involves studying all currently recognized diseases – so called ‘phenome wide’ approaches. In order to do this efficiently phenomics approaches require the creation of computable definitions of diseases, health states and traits, including temporal components of these (i.e. change and rate of change over time). It covers the full spectrum of health and disease across the entire life course and is relevant to a wide range of potential stakeholders and beneficiaries. 

### The challenge

A primary reason for using data from EHR is the creation of phenotype algorithms to identify disease status, onset and progression. Phenotyping (describing the characteristics of disease) however is challenging as the data are collected for different purposes, have variable data quality and often require significant harmonisation. While considerable effort goes into these algorithms, there is no consistent methodology for creating and evaluating them and no centralised repository for depositing and sharing them.

### The solution

We will create a national platform for dissemination of citable algorithms (incl. validations) and tools which will reduce duplication of effort and improve research reproducibility. We will explore methods for creating computable representations of algorithms for integration into actionable analytics for healthcare. Finally, we will fundamentally shift the EHR cultural landscape by a robust incentivisation programme, providing guidelines on best practices, cross-disciplinary training, and ensuring alignment with other international initiatives.

### Impact and outcomes

Though this project, we will deliver a fundamental step-change in the current EHR community in the UK by bringing together health data scientists, clinicians, computer scientists, public health experts and data curators under the FAIR principles (www.force11.org). The National Phenomics Resource will facilitate the dissemination and re-use of algorithms, tools and methods by the community. By establishing a national standard for creating, evaluating and representing phenotypes, we will accelerate the impact of discovery through increased transparency and replicability and maximise the usability and value of existing data repositories to new users. Finally, we will take the first steps towards establishing computational biomedical knowledge objects (e.g. guidelines with embedded phenotypes endorsed by NICE) which will enable the creation of actionable health analytics in the NHS.


## About the resource

### Electronic health records

When patients interact with physicians, or are admitted into hospital, information is collected electronically on their symptoms, diagnoses, laboratory test results, and prescriptions and stored in **Electronic Health Records** (EHR). EHR are a valuable resource for researchers and clinicians as they provide comprehesive information about a patients health, and healthcare, over long periods of time. 

### Phenotyping algoritms
A primary use-case for EHR is the creation of **phenotyping algorithms** used to identify disease status, onset and progression or extraction of information on risk factors or biomarkers. These complex algorithms can enable researchers to extract information from EHR, statistically analyze it and use the findings to improve human health. While considerable effort goes into creating these algorithms, there is no consistent methodology for creating and evaluating them and no centralised repository for depositing and sharing them.

### What is the Phenotype Portal?

The **HDR UK Phenotype Portal** will facilitate the dissemination and re-use of algorithms, tools and methods by the community by providing a national resource for curating such algorithms and their associated metadata.

## Technical documentation

### Phenotype Portal Inclusion Criteria

For an algorithm to be **included in the Phenotype Portal**, it must satisfy the following criteria:

* Define a disease (e.g. hypertension), life style risk factor (e.g. smoking) or biomarker (e.g. blood pressure)
* Derive information from one or more electronic health record data sources. This can include national and local sources. The definition of EHR includes administrative data such as billing/claims data, and clinical audits.
* Have one or more peer-reviewed outputs associated with it e.g. journal publication, scientific conferences, policy white papers etc.
* Provide evidence of how the phenotyping algorithm was validated.

### Specification

Phenotyping algorithms are stored in the Phenotype Portal usign a combination of YAML, CSV and markdown files. There are two main components to each algorothm: a) the phenotype definition file (which is in YAML and markdown) and, b) one or more teminology files (also known as codelists) which are stored as CSV files. The section below provides information on their schema and contents.

<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" width="481px" viewBox="-0.5 -0.5 481 241" content="&lt;mxfile host=&quot;Electron&quot; modified=&quot;2020-07-17T10:25:32.250Z&quot; agent=&quot;5.0 (Macintosh; Intel Mac OS X 10_15_4) AppleWebKit/537.36 (KHTML, like Gecko) draw.io/13.2.4 Chrome/83.0.4103.104 Electron/9.0.4 Safari/537.36&quot; etag=&quot;rJQazkSRR-_YdsYiEPns&quot; version=&quot;13.2.4&quot; type=&quot;device&quot;&gt;&lt;diagram id=&quot;prtHgNgQTEPvFCAcTncT&quot; name=&quot;Page-1&quot;&gt;7Vjvb9o6FP1r+LiJJBDox0LbVVqZqjFtn01ySfzm2MwxDeyv373ESXCSUrQNqe+9SkjEx9e/7jm+HDII5tnug2abdKFiEAN/GO8Gwc3A9z1vGOIXIXuLDIdBiSSaxxZrgCX/CVWgRbc8htwJNEoJwzcuGCkpITIOxrRWhRu2VsJddcMS6ADLiIku+o3HJi3RqT9p8HvgSVqt7IVXZU/GqmB7kjxlsSqOoOB2EMy1UqZ8ynZzEJS9Ki/luLtneuuNaZDmnAHxp93+08dJNJmuHoqnPIbF/fidZ6d5YmJrT3wrMI9aSR4hfg9M4Dn84WeIlI5zfHpMQSqz33CZUI5FojQ3aWYPafZV5vKCZ4JJbM1SkwkEPXzMDdPG0owbxj4c/lNJw6qIiBpcgv6y31CU0UBzJILlxCWN6R69OgZoA7sjyKbiA6gMjN5jiO0dWVasLqe2WTQcjyosPeK3HsesrpJ65ib1+GCz389EolarO7j/lq9md/+wXTj7WqzfeaMOE1WmgS4QrLnkhis5IJ7xWgUepWLNMd8nUr/GbC5tzyG7KRfxA9urLZ0I2Yi+V60uFcdkjexqYq6E0ghIVXJbD1rSZJYhDTkOe6wY8lrQgu2cwAeWGwtESgi2yfmq3nLGdMLlTBmjMkcAHbZdTZwQ/LOy8KauLoKuLrxxjy6uTsjCLoY3yDCZEF31auH4xdVGPau1RYh3FLRkBmZqK+mStrRYn/MP5DnuyHMBhsXMsI78kBRzUI9W36Ellx4FMcETiU0BaxpGrHIswNcWNmpDk21YhBXn4RBzM2qQzzYtBCkcuxaHIpvyOAZJAlMG91iqiaSzUVyaQ97GM/xgJufD9+PBGDc+x7bXtPFD4drMlcSzYE2idQClWgDJ9TwVnrjsXRXuXX5fUh0BlylGYYdtTIKhQ72R/ZfJDv0zyZ5eiOzKoByR3WEZYnRFtglipYrbBpgdAOyoyKx+Oa7JfzXUg4xbiKZyBbFT1Gkl1+5h+YdT+a0S89u1X4Nghj+5y56o5I+kqqaK++ORU8U9v1Wec7XVEdhRf780+10PhwZBkGhX+JDQw5ycOc9p16VjKPtxvTqkw3mRcgNLvHjULtDfu06uuskRJh10z13O8FYe9EEO7g6NNznGciwhC/XUABKOFXUzmOB2wh9b8sazRns1NAiuj/pdPTZBeMfrxpEg+2c5SLJ/bC3cs0ZObi5pUK5cx+CFPT8Vw57qEV7Kt/pdY/Cmvv+q+gLv1clv+ia//438/OGrk1/XKL8m73RmwnG7B4tyxj+Cl93Y+FWZrO5ErX/4Xlsb5Qkv59b8f41izjbgF/LVVy7l/vA3KQ/C1kTt9yfPUI75Y/ujMPtv8tkNB74rrdYbWXwoZzxTT9hs3g6X4c1L9uD2Fw==&lt;/diagram&gt;&lt;/mxfile&gt;" onclick="(function(svg){var src=window.event.target||window.event.srcElement;while (src!=null&amp;&amp;src.nodeName.toLowerCase()!='a'){src=src.parentNode;}if(src==null){if(svg.wnd!=null&amp;&amp;!svg.wnd.closed){svg.wnd.focus();}else{var r=function(evt){if(evt.data=='ready'&amp;&amp;evt.source==svg.wnd){svg.wnd.postMessage(decodeURIComponent(svg.getAttribute('content')),'*');window.removeEventListener('message',r);}};window.addEventListener('message',r);svg.wnd=window.open('https://app.diagrams.net/?client=1&amp;lightbox=1&amp;edit=_blank');}}})(this);" style="cursor:pointer;max-width:100%;max-height:241px;"><defs><clipPath id="mx-clip-184-75-142-22-0"><rect x="184" y="75" width="142" height="22"/></clipPath><clipPath id="mx-clip-184-97-142-28-0"><rect x="184" y="97" width="142" height="28"/></clipPath></defs><g><path d="M 0 20 L 0 0 L 480 0 L 480 20" fill="#ffffff" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/><path d="M 0 20 L 0 240 L 480 240 L 480 20" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="none"/><path d="M 0 20 L 480 20" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="none"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 10px; margin-left: 240px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: none; font-weight: bold; white-space: nowrap; ">Electronic Health Records Phenotyping algorithm</div></div></div></foreignObject><text x="240" y="14" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle" font-weight="bold">Electronic Health Records Phenotyping algorithm</text></switch></g><path d="M 180 70 L 180 30 L 330 30 L 330 70" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="none"/><path d="M 180 70 L 180 120 L 330 120 L 330 70" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="none"/><path d="M 180 70 L 330 70" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="none"/><g fill="#000000" font-family="Helvetica" font-weight="bold" text-anchor="middle" font-size="12px"><text x="254.5" y="47.5">Phenotype definition </text><text x="254.5" y="61.5">file</text></g><g fill="#000000" font-family="Helvetica" clip-path="url(#mx-clip-184-75-142-22-0)" font-size="12px"><text x="185.5" y="87.5">Metadata</text></g><g fill="#000000" font-family="Helvetica" clip-path="url(#mx-clip-184-97-142-28-0)" font-size="12px"><text x="185.5" y="109.5">Content</text></g><path d="M 254 120 L 254 140 L 255 140 L 255 160" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="none"/><rect x="95" y="160" width="100" height="60" fill="#ffffff" stroke="#000000" pointer-events="none"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 190px; margin-left: 96px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: none; white-space: normal; word-wrap: normal; "><b>Codelist file</b></div></div></div></foreignObject><text x="145" y="194" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">Codelist file</text></switch></g><rect x="315" y="160" width="100" height="60" fill="#ffffff" stroke="#000000" pointer-events="none"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 190px; margin-left: 316px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: none; white-space: normal; word-wrap: normal; "><b>Codelist file</b></div></div></div></foreignObject><text x="365" y="194" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">Codelist file</text></switch></g><rect x="205" y="160" width="100" height="60" fill="#ffffff" stroke="#000000" pointer-events="none"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 190px; margin-left: 206px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: none; white-space: normal; word-wrap: normal; "><b>Codelist file</b></div></div></div></foreignObject><text x="255" y="194" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">Codelist file</text></switch></g><path d="M 255 120 L 255 140 L 365 140 L 365 160" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="none"/><path d="M 254 120 L 254 140 L 145 140 L 145 160" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="none"/></g><switch><g requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"/><a transform="translate(0,-5)" xlink:href="https://desk.draw.io/support/solutions/articles/16000042487" target="_blank"><text text-anchor="middle" font-size="10px" x="50%" y="100%">Viewer does not support full SVG 1.1</text></a></switch></svg>

### File naming

All phenotype definition files associated with a phenotype use a common naming pattern:

```
AUTHORSURNAME_NAME_UUID.md 
```

for example: `axson_bronchiestasis_ZckoXfUWNXn8Jn7fdLQuxj.md`

Phenotype files are stored in the [_phenotypes directory](https://github.com/spiros/hdr-caliber-phenome-portal/tree/master/_phenotypes).


Similarly, code list files follow a similar pattern:

```
NAME_UUID_TERMINOLOGY.csv
```

for example: `axson_bronchiestasis_ZckoXfUWNXn8Jn7fdLQuxj_ICD10.csv`

Codelist files are stored in the [codelists directory](https://github.com/spiros/hdr-caliber-phenome-portal/tree/master/_data/codelists).


### Phenotype definition file

The phenotype definition file is a markdown file with a YAML header. The YAML header is used to record metadata fields capturing information about the algorithm, the data sources, controlled clinical terminologies and other information. 

For example, the code snippet below displays the metadata associated with the [bronchiestasis](https://portal.caliberresearch.org/phenotypes/axson-bronchiestasis-zckoxfuwnxn8jn7fdlquxj) phenotyping algorithm submitted by the HDR UK BREATHE Hub (you can view the [raw file](https://raw.githubusercontent.com/spiros/hdr-caliber-phenome-portal/master/_phenotypes/axson_bronchiestasis_ZckoXfUWNXn8Jn7fdLQuxj.md) directly on the repository.)

```yaml
title: Bronchiestasis
name: Bronchiestasis
phenotype_id: ZckoXfUWNXn8Jn7fdLQuxj 
type: Disease or Syndrome
group: Respiratory
data_sources: 
    - Clinical Practice Research Datalink GOLD
    - Clinical Practice Research Datalink Aurum
    - Hospital Episode Statistics APC for CPRD GOLD
    - Hospital Episode Statistics APC for CPRD Aurum
    - Death Registration data for CPRD GOLD
    - Death Registration data for CPRD Aurum
    - UK Biobank
clinical_terminologies: 
    - Read Version 2
    - SNOMED-CT
    - ICD-10
    - ICD-11
validation: 
    - prognostic
codelists:
    - axson_bronchiestasis_ZckoXfUWNXn8Jn7fdLQuxj_ICD10.csv
    - axson_bronchiestasis_ZckoXfUWNXn8Jn7fdLQuxj_ICD11.csv
    - axson_bronchiestasis_ZckoXfUWNXn8Jn7fdLQuxj_SNOMEDCT.csv
    - axson_bronchiestasis_ZckoXfUWNXn8Jn7fdLQuxj_UKBIOBANK.csv
valid_event_data_range: 01/01/2001 - 31/12/2019
sex: 
    - Female
    - Male
author: 
    - Eleanor L Axson
    - Jennifer K Quint
publications: 
status: BETA
date: 2019-06-20
modified_date: 2019-06-20
version: 1
```

The metadata fields required are the following:

* **title** (string): Phenotype (long) name
* **name (string)**: Phenotype (short) name 
* **data_sources** (list of strings): Names of data sources that phenotype sources information from. These should be identical, if possible, to the names used to identify individual datasets in the [HDR Gateway](https://www.healthdatagateway.org/).
* **clinical_terminologies** (list of strings): List of controlled clinical terminologies that are used by the phenotype algorithm.
* **validation** (list of strings): evidence of validation used as evidence of phenotype robustness - valid values:
    * _prognostic_: the ability to replicate known prognostic associations
    * _aetiologic_: the ability to replicate known associations with risk factors
    * _genetic_ : the abity to replicate associations with known regions or variants
    * _cross-source_: has the algorithm been evaluated in a similar external data source
    * _casenote review_ : has the algorithm been validated through manual review of clinical notes (this usually would result to PPV, NPV values)
    * _cross-country_ : has the algorithm been evaluated in a similar external healthcare system
* **codelists** (list of strings): (unordered) list of CSV terminology files associated with the phenotype
* **phenotype_id** (list of strings): Unique universal phenotype identifier, generated using the `shortuuid` [Python module](https://pypi.org/project/shortuuid/).
* **group** (string): Disease group for phenotype
* **valid_event_data_range** (list of strings): DD/MM/YYYY date range for events
* **sex** (list of strings): list of sexes valid for the phenotype
* **author** (list of strings): list of phenotype authors 
* **publications** (list of strings): list of publications
* **status** (string): 'DRAFT' or 'FINAL' status
* **date** (string): date created
* **modified_date** (string): date last modified
* **version** (integer): integer version of phenotype, default '1'

### Terminology files (codelists)

Codelist files are specified as CSV files with one term per row - for example:

```
ICD-10 code,ICD-10 term
J47,Bronchiectasis
```

### How to submit data

You can download a [**sample template file**](https://raw.githubusercontent.com/spiros/hdr-caliber-phenome-portal/develop/sample_phenotype_1233456.md) from the repository: 

If you have a phenotyping algorithm that meets the eligibility requirements, we invite you to submit your data by one of the following ways:

* by 📫 **email** <a href="mailto:s.denaxas[@]ucl.ac.uk">s.denaxas at ucl.ac.uk</a>
* by 🐙 **pull request (PR)** on the [GitHub repository](https://github.com/spiros/hdr-caliber-phenome-portal)
* by ⬆ [**Google form**](https://forms.gle/J5dm94jeT6MG1StP9)




