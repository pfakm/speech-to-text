---

copyright:
  years: 2015, 2017
lastupdated: "2017-12-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# Parameter summary
{: #summary}

This page summarizes all of the parameters available for speech recognition. Each parameter includes a link to its description in [Input features](/docs/services/speech-to-text/input.html) or [Output features](/docs/services/speech-to-text/output.html). For complete details about all methods of the {{site.data.keyword.speechtotextshort}} service, see the [API reference ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/watson/developercloud/speech-to-text/api/v1/){: new_window}.
{: shortdesc}

When making a request, keep the following in mind:

-   Method names are case-sensitive.
-   HTTP request headers are case-insensitive.
-   HTTP query parameters are case-sensitive.
-   JSON field names are case-sensitive.

You need to specify only the input audio and its format (`Content-Type`); all other parameters are optional. If you specify an invalid query parameter or JSON field as part of the input for a recognition request, the response includes a `warnings` field that describes the invalid argument. The request succeeds despite the warnings.

## acoustic_customization_id

An optional customization ID for a custom acoustic model that is adapted for the acoustic characteristics of your environment and speakers. By default, no custom model is used. See [Custom models](/docs/services/speech-to-text/input.html#custom).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Beta for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Query parameter of <code>/v1/recognize</code> connection request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## Content-Type

A required audio format (MIME type) that specifies the format of the audio data that you pass to the service. See [Audio formats](/docs/services/speech-to-text/audio-formats.html).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      <code>content-type</code> parameter of JSON <code>start</code>
      message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Request header of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Request header of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Request header of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## customization_id

An optional customization ID for a custom language model that includes terminology from your domain. By default, no custom model is used. See [Custom models](/docs/services/speech-to-text/input.html#custom).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for US English, UK English, Japanese, and Spanish
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Query parameter of <code>/v1/recognize</code> connection request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## customization_weight

An optional double between 0.0 and 1.0 that indicates the relative weight that the service gives to words from a custom language model compared to those from the base vocabulary. The default is 0.3 unless a different weight was specified when the custom language model was trained. See [Custom models](/docs/services/speech-to-text/input.html#custom).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for US English, UK English, Japanese, and Spanish
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Query parameter of <code>/v1/recognize</code> connection request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## inactivity_timeout

An optional integer that specifies the number of seconds for the service's inactivity timeout; use `-1` to indicate infinity. The default is 30 seconds. See [Inactivity timeout](/docs/services/speech-to-text/input.html#timeouts).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## interim_results

An optional boolean that directs the service to return intermediate hypotheses that are likely to change before the final transcript. By default (`false`), interim results are not returned. See [Interim results](/docs/services/speech-to-text/output.html#interim).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Not supported
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of
      <code>GET /v1/sessions/{session_id}/observe_result</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Not supported
    </td>
  </tr>
</table>

## keywords

An optional array of keyword strings that the service spots in the input audio. By default, keyword spotting is not performed. See [Keyword spotting](/docs/services/speech-to-text/output.html#keyword_spotting).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Beta for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## keywords_threshold

An optional double between 0.0 and 1.0 that indicates the minimum threshold for a positive keyword match. By default, keyword spotting is not performed. See [Keyword spotting](/docs/services/speech-to-text/output.html#keyword_spotting).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Beta for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## max_alternatives

An optional integer that specifies the maximum number of alternative hypotheses that the service returns. By default, the service returns a single final hypothesis. See [Maximum alternatives](/docs/services/speech-to-text/output.html#max_alternatives).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## model

An optional model that specifies the language in which the audio is spoken and the rate at which it was sampled, broadband or narrowband. By default, `en-US_BroadbandModel` is used. See [Language and models](/docs/services/speech-to-text/input.html#models).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Query parameter of <code>/v1/recognize</code> connection request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## profanity_filter

An optional boolean that indicates whether the service censors profanity from a transcript. By default (`true`), profanity is filtered from the transcript. See [Profanity filtering](/docs/services/speech-to-text/output.html#profanity_filter).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for US English
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## smart_formatting

An optional boolean that indicates whether the service converts dates, times, numbers, currency, and similar values into more conventional representations in the final transcript. By default (`false`), smart formatting is not performed. See [Smart formatting](/docs/services/speech-to-text/output.html#smart_formatting).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Beta for US English
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## speaker_labels

An optional boolean that indicates whether the service identifies which individuals spoke which words in a multi-participant exchange. By default (`false`), speaker labels are not returned. See [Speaker labels](/docs/services/speech-to-text/output.html#speaker_labels).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Beta for US English, Japanese, and Spanish
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## timestamps

An optional boolean that indicates whether the service produces timestamps for the words of the transcript. By default (`false`), timestamps are not returned. See [Word timestamps](/docs/services/speech-to-text/output.html#word_timestamps).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## Transfer-Encoding

An optional value of `chunked` that causes the audio to be streamed to the service. By default, audio is sent all at once as a one-shot delivery. See [Audio transmission](/docs/services/speech-to-text/input.html#transmission).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Not applicable; always streamed
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Request header of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Request header of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Request header of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## version

An optional version of a base model. The parameter is intended primarily for use with custom models that have been updated for a new base model, but it can be used without a custom model. The default value depends on whether the parameter is used with or without a custom model. See [Base model version](/docs/services/speech-to-text/input.html#version).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Query parameter of <code>/v1/recognize</code> connection request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## watson-token

An optional authentication token that makes authenticated requests to the service without embedding your service credentials in every call. By default, service credentials must be passed with each request. See [Authentication tokens and request logging](/docs/services/speech-to-text/input.html#common).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Query parameter of <code>/v1/recognize</code> connection request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of each request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of each request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of each request
    </td>
  </tr>
</table>

## word_alternatives_threshold

An optional double between 0.0 and 1.0 that specifies the threshold at which the service reports acoustically similar alternatives for words of the input audio. By default, word alternatives are not returned. See [Word alternatives](/docs/services/speech-to-text/output.html#word_alternatives).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Beta for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## word_confidence

An optional boolean that indicates whether the service provides confidence measures for the words of the transcript. By default (`false`), word confidence measures are not returned. See [Word confidence](/docs/services/speech-to-text/output.html#word_confidence).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Parameter of JSON <code>start</code> message
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognize</code> method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/sessions/{session_id}/recognize</code>
      method
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Query parameter of <code>POST /v1/recognitions</code> method
    </td>
  </tr>
</table>

## X-Watson-Authorization-Token

An optional authentication token that makes authenticated requests to the service without embedding your service credentials in every call. By default, service credentials must be passed with each request. See [Authentication tokens and request logging](/docs/services/speech-to-text/input.html#common).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      Not available; use the <code>watson-token</code> query parameter
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Request header of each request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Request header of each request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Request header of each request
    </td>
  </tr>
</table>

## X-Watson-Learning-Opt-Out

An optional boolean that indicates whether you opt out of the request logging that {{site.data.keyword.IBM_notm}} performs to improve the service for future users. By default (`false`), request logging is performed. See [Authentication tokens and request logging](/docs/services/speech-to-text/input.html#common).

<table>
  <tr>
    <td style="text-align:left; width:30%">
      **Availability**
    </td>
    <td style="text-align:left">
      Generally available for all languages
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **WebSocket**
    </td>
    <td style="text-align:left">
      <code>x-watson-learning-opt-out</code> query parameter of
      <code>/v1/recognize</code> connection request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessionless**
    </td>
    <td style="text-align:left">
      Request header of each request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP sessions**
    </td>
    <td style="text-align:left">
      Request header of each request
    </td>
  </tr>
  <tr>
    <td style="text-align:left">
      **HTTP asynchronous**
    </td>
    <td style="text-align:left">
      Request header of each request
    </td>
  </tr>
</table>
