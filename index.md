---

copyright:
  years: 2018, 2019
lastupdated: "2019-03-28"

keywords: supported frameworks, models, model types, limitations, limits

subcollection: ai-openscale

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:pre: .pre}
{:codeblock: .codeblock}
{:download: .download}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# About
{: #in-ov}

{{site.data.keyword.aios_full}} is an enterprise-grade environment for AI-infused applications, providing enterprises visibility into how AI is being built, used, and delivering return on investment, at the scale of your business.
{: shortdesc}

<p>&nbsp;</p>

## Implementation
{: #in-imp}

Here's how you will implement {{site.data.keyword.aios_short}}:

- **Configure {{site.data.keyword.aios_short}}**: With the easy-to-use graphical environment, [set up a payload logging database](/docs/services/ai-openscale?topic=ai-openscale-connect-db), and the [Watson Machine Learning instance](/docs/services/ai-openscale?topic=ai-openscale-wml-connect) where your AI models and deployments are stored.

- **Work with monitors**: For each deployment, configure how {{site.data.keyword.aios_short}} will monitor that deployment. You can monitor for:

    - [Fairness](/docs/services/ai-openscale?topic=ai-openscale-mf-monitor)
    - [Accuracy](/docs/services/ai-openscale?topic=ai-openscale-acc-monitor)

- **View and edit monitored data**: The {{site.data.keyword.aios_short}} [dashboard](/docs/services/ai-openscale?topic=ai-openscale-io-ov) lets you easily view key insights and identify issues for your deployments. Visualization of individual data points for each monitored feature provides additional detail.

<p>&nbsp;</p>

## Limitations
{: #in-lim}

- The current release only supports one database, one Watson Machine Learning instance, and one instance of {{site.data.keyword.aios_short}}

- The database and Watson Machine Learning instance must be deployed in the same {{site.data.keyword.cloud_notm}} account.

- The Lite (free) plan has the following monthly limits:

    - Two deployed models monitored
    - 20 transactions explained
    - 50,000 payload records (cumulative)
    - 50,000 feedback records (cumulative)

- {{site.data.keyword.aios_short}} uses a PostgreSQL or Db2 database to store model deployment output and retraining data. Lite Db2 plans are not currently supported.

- There is a license limit of 20 deployed models per instance of {{site.data.keyword.aios_short}}.

- Currently, explanations cannot be generated for images which are greater than 1 MB in size.

<p>&nbsp;</p>

## Supported model types
{: #in-mod}

Table 1. Model support details

| Algorithms | **Fairness** | **Auto-debias** | **Explain** | **Accuracy** |
|:---|:---:|:---:|:---:|:---:|
| **Structured Classification** | Yes | Yes<sup>1</sup> | Yes | Yes |
| **Structured Regression**     | Yes | No | Yes | Yes |
| **Text Classification**       | No | No | Yes | No |
| **Image Classification**      | No | No | Yes | No ||
{: caption="Model support details" caption-side="top"}

<sup>1</sup> If your model / framework outputs prediction probabilities

<p>&nbsp;</p>

## Supported machine learning engines and frameworks
{: #in-fram}

The {{site.data.keyword.aios_short}} service supports the following machine learning engines. Each runtime supports models that are created in the following frameworks as described in the list of [Supported model types](#in-mod).

- [{{site.data.keyword.pm_full}}](/docs/services/ai-openscale?topic=ai-openscale-frmwrks-wml#frmwrks-wml) 
- [Azure ML Studio](/docs/services/ai-openscale?topic=ai-openscale-frmwrks-azure#frmwrks-azure)
- [AWS Sagemaker](/docs/services/ai-openscale?topic=ai-openscale-frmwrks-aws-sage#frmwrks-aws-sage)
- [Custom](/docs/services/ai-openscale?topic=ai-openscale-frmwrks-custom#frmwrks-custom)


- [SAS AI Studio](/docs/services/ai-openscale?topic=ai-openscale-frmwrks-sas#frmwrks-sas)
{: download}
- [Google Cloud ML Engine](/docs/services/ai-openscale?topic=ai-openscale-frmwrks-google#frmwrks-google)
{: download}
- [SPSS C&DS (ICP only)](/docs/services/ai-openscale?topic=ai-openscale-frmwrks-spss#frmwrks-spss)
{: download}

Full support includes the following features for the specific framework, problem, and data type:

- Payload logging	
- Feedback logging	
- Performance	Accuracy	
- Run-time bias detection	
- Explainability	
- Auto-Debias

<p>&nbsp;</p>

## Browser support
{: #in-brw}

The {{site.data.keyword.aios_short}} service tooling requires the same level of browser software as is required by {{site.data.keyword.cloud_notm}}. See the {{site.data.keyword.cloud_notm}} [Prerequisites](/docs/overview?topic=overview-prereqs-platform#browsers-platform) topic for details.

<p>&nbsp;</p>

## ModelOps CLI tool
{: #in-mop}

The [{{site.data.keyword.aios_short}} CLI model operations tool ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://github.com/IBM-Watson/aiopenscale-modelops-cli){: new_window} allows you to execute tasks related to the lifecycle management of machine learning models. This tool is complementary to the {{site.data.keyword.cloud_notm}} CLI tool, augmented with the [machine learning plugin ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/DSXDOC/analyze-data/ml_dlaas_environment.html){: new_window}.

<p>&nbsp;</p>

## Python client
{: #in-pyc}

The [{{site.data.keyword.aios_short}} Python client ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ai-openscale-python-client.mybluemix.net/){: new_window} is a Python library that allows you to work directly with the {{site.data.keyword.aios_short}} service on {{site.data.keyword.cloud_notm}}. You can use the Python client, instead of the {{site.data.keyword.aios_short}} client UI, to directly configure a logging database, bind your machine learning engine, and select and monitor deployments. For examples using the Python client in this way, see the [{{site.data.keyword.aios_short}} sample notebooks ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://github.com/pmservice/ai-openscale-tutorials/tree/master/notebooks).

<p>&nbsp;</p>

## Next steps
{: #in-next}

- [Get started](/docs/services/ai-openscale?topic=ai-openscale-gettingstarted) with the service.
- View the [API Reference material ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/apidocs/ai-openscale){: new_window}.

Still have questions? [Contact IBM ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/account/reg/us-en/signup?formid=MAIL-watson){: new_window}.
