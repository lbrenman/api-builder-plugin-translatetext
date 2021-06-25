# API Builder Plugin for AWS Translate

[**Axway API Builder**](https://docs.axway.com/bundle/API_Builder_4x_allOS_en/page/api_builder.html) flow-node that implements [**AWS Comprehend**](https://docs.aws.amazon.com/comprehend/index.html) for Natural Language Processing ([**NLP**](https://en.wikipedia.org/wiki/Natural_language_processing)): *api-builder-plugin-translatetext*

## About flow-nodes

Flow-nodes are used within Axway API Builder's flow editor that is a low-code / no-code solution to designing and developing services
that integrate to many different connected components, such as databases and APIs.

## Install

After creating your [**API Builder Project**](https://docs.axway.com/bundle/API_Builder_4x_allOS_en/page/api_builder_getting_started_guide.html), you can install this plugin using npm:

```
npm install api-builder-plugin-translatetext
```

> Note that this command will install from npm. If you want to install locally, then provide the full path to the plugin folder

Before launching your API Builder app that uses this plugin, you must set the following two environment variables as per the [**AWS SDK for JavaScript online docs**](https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/loading-node-credentials-environment.html):

* AWS_ACCESS_KEY_ID
* AWS_SECRET_ACCESS_KEY

## Use

Find the plugin in the NLP group in the Flow-Nodes panel. Drag onto the canvas and select the desired method and provide the input Text and wire up to the rest of your flow as shown below:

![](https://i.imgur.com/o6cPHdf.png)

## Methods

The currently implemented methods are described below.

### Translate Text

AWS docs are [**here**](https://docs.aws.amazon.com/translate/latest/dg/API_TranslateText.html)

Provide the *Text* input and the *Target Language Code* and the output will be similar to below:

Text = "Hello World"

Target Language Code = ja (Japanese)

```
{
  "TranslatedText": "ハローワールド",
  "SourceLanguageCode": "en",
  "TargetLanguageCode": "ja"
}
```

> Note that AWS will automatically detect the input language
