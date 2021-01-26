Siddhi IO HTTP
======================================

  [![Jenkins Build Status](https://wso2.org/jenkins/job/siddhi/job/siddhi-io-http/badge/icon)](https://wso2.org/jenkins/job/siddhi/job/siddhi-io-http/)
  [![GitHub Release](https://img.shields.io/github/release/siddhi-io/siddhi-io-http.svg)](https://github.com/siddhi-io/siddhi-io-http/releases)
  [![GitHub Release Date](https://img.shields.io/github/release-date/siddhi-io/siddhi-io-http.svg)](https://github.com/siddhi-io/siddhi-io-http/releases)
  [![GitHub Open Issues](https://img.shields.io/github/issues-raw/siddhi-io/siddhi-io-http.svg)](https://github.com/siddhi-io/siddhi-io-http/issues)
  [![GitHub Last Commit](https://img.shields.io/github/last-commit/siddhi-io/siddhi-io-http.svg)](https://github.com/siddhi-io/siddhi-io-http/commits/master)
  [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

The **siddhi-io-http extension** is an extension to <a target="_blank" href="https://wso2.github.io/siddhi">Siddhi</a> that receives and publishes events via HTTP and HTTPS transports, calls external services, and serves incoming requests and provide synchronous responses.

For information on <a target="_blank" href="https://siddhi.io/">Siddhi</a> and it's features refer <a target="_blank" href="https://siddhi.io/redirect/docs.html">Siddhi Documentation</a>. 

## Download

* Versions 2.x and above with group id `io.siddhi.extension.*` from <a target="_blank" href="https://mvnrepository.com/artifact/io.siddhi.extension.io.http/siddhi-io-http/">here</a>.
* Versions 1.x and lower with group id `org.wso2.extension.siddhi.*` from <a target="_blank" href="https://mvnrepository.com/artifact/org.wso2.extension.siddhi.io.http/siddhi-io-http">here</a>.

## Latest API Docs 

Latest API Docs is <a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4">2.2.4</a>.

## Features

* <a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4/#http-sink">http</a> *(<a target="_blank" href="http://siddhi.io/en/v5.1/docs/query-guide/#sink">Sink</a>)*<br> <div style="padding-left: 1em;"><p><p style="word-wrap: break-word;margin: 0;">HTTP sink publishes messages via HTTP or HTTPS protocols using methods such as POST, GET, PUT, and DELETE on formats <code>text</code>, <code>XML</code> and <code>JSON</code>. It can also publish to endpoints protected by basic authentication or OAuth 2.0.</p></p></div>
* <a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4/#http-call-sink">http-call</a> *(<a target="_blank" href="http://siddhi.io/en/v5.1/docs/query-guide/#sink">Sink</a>)*<br> <div style="padding-left: 1em;"><p><p style="word-wrap: break-word;margin: 0;">The http-call sink publishes messages to endpoints via HTTP or HTTPS protocols using methods such as POST, GET, PUT, and DELETE on formats <code>text</code>, <code>XML</code> or <code>JSON</code> and consume responses through its corresponding http-call-response source. It also supports calling endpoints protected with basic authentication or OAuth 2.0.</p></p></div>
* <s><a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4/#http-request-sink">http-request</a> *(<a target="_blank" href="http://siddhi.io/en/v5.1/docs/query-guide/#sink">Sink</a>)*</s><br> <div style="padding-left: 1em;"><p><p style="word-wrap: break-word;margin: 0;">_(Use http-call sink instead)._<br>The http-request sink publishes messages to endpoints via HTTP or HTTPS protocols using methods such as POST, GET, PUT, and DELETE on formats <code>text</code>, <code>XML</code> or <code>JSON</code> and consume responses through its corresponding http-response source. It also supports calling endpoints protected with basic authentication or OAuth 2.0.</p></p></div>
* <s><a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4/#http-response-sink">http-response</a> *(<a target="_blank" href="http://siddhi.io/en/v5.1/docs/query-guide/#sink">Sink</a>)*</s><br> <div style="padding-left: 1em;"><p><p style="word-wrap: break-word;margin: 0;">_(Use http-service-response sink instead)._<br>The http-response sink send responses of the requests consumed by its corresponding http-request source, by mapping the response messages to formats such as <code>text</code>, <code>XML</code> and <code>JSON</code>.</p></p></div>
* <a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4/#http-service-response-sink">http-service-response</a> *(<a target="_blank" href="http://siddhi.io/en/v5.1/docs/query-guide/#sink">Sink</a>)*<br> <div style="padding-left: 1em;"><p><p style="word-wrap: break-word;margin: 0;">The http-service-response sink send responses of the requests consumed by its corresponding http-service source, by mapping the response messages to formats such as <code>text</code>, <code>XML</code> and <code>JSON</code>.</p></p></div>
* <a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4/#http-source">http</a> *(<a target="_blank" href="http://siddhi.io/en/v5.1/docs/query-guide/#source">Source</a>)*<br> <div style="padding-left: 1em;"><p><p style="word-wrap: break-word;margin: 0;">HTTP source receives POST requests via HTTP and HTTPS protocols in format such as <code>text</code>, <code>XML</code> and <code>JSON</code>. It also supports basic authentication to ensure events are received from authorized users/systems.<br>The request headers and properties can be accessed via transport properties in the format <code>trp:&lt;header&gt;</code>.</p></p></div>
* <a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4/#http-call-response-source">http-call-response</a> *(<a target="_blank" href="http://siddhi.io/en/v5.1/docs/query-guide/#source">Source</a>)*<br> <div style="padding-left: 1em;"><p><p style="word-wrap: break-word;margin: 0;">The http-call-response source receives the responses for the calls made by its corresponding http-call sink, and maps them from formats such as <code>text</code>, <code>XML</code> and <code>JSON</code>.<br>To handle messages with different http status codes having different formats, multiple http-call-response sources are allowed to associate with a single http-call sink.<br>It allows accessing the attributes of the event that initiated the call, and the response headers and properties via transport properties in the format <code>trp:&lt;attribute name&gt;</code> and <code>trp:&lt;header/property&gt;</code> respectively.</p></p></div>
* <s><a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4/#http-request-source">http-request</a> *(<a target="_blank" href="http://siddhi.io/en/v5.1/docs/query-guide/#source">Source</a>)*</s><br> <div style="padding-left: 1em;"><p><p style="word-wrap: break-word;margin: 0;">_(Use http-service source instead)._<br>The http-request source receives POST requests via HTTP and HTTPS protocols in format such as <code>text</code>, <code>XML</code> and <code>JSON</code> and sends responses via its corresponding http-response sink correlated through a unique <code>source.id</code>.<br>For request and response correlation, it generates a <code>messageId</code> upon each incoming request and expose it via transport properties in the format <code>trp:messageId</code> to correlate them with the responses at the http-response sink.<br>The request headers and properties can be accessed via transport properties in the format <code>trp:&lt;header&gt;</code>.<br>It also supports basic authentication to ensure events are received from authorized users/systems.</p></p></div>
* <s><a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4/#http-response-source">http-response</a> *(<a target="_blank" href="http://siddhi.io/en/v5.1/docs/query-guide/#source">Source</a>)*</s><br> <div style="padding-left: 1em;"><p><p style="word-wrap: break-word;margin: 0;">_(Use http-call-response source instead)._<br>The http-response source receives the responses for the calls made by its corresponding http-request sink, and maps them from formats such as <code>text</code>, <code>XML</code> and <code>JSON</code>.<br>To handle messages with different http status codes having different formats, multiple http-response sources are allowed to associate with a single http-request sink. It allows accessing the attributes of the event that initiated the call, and the response headers and properties via transport properties in the format <code>trp:&lt;attribute name&gt;</code> and <code>trp:&lt;header/property&gt;</code> respectively.</p></p></div>
* <a target="_blank" href="https://siddhi-io.github.io/siddhi-io-http/api/2.2.4/#http-service-source">http-service</a> *(<a target="_blank" href="http://siddhi.io/en/v5.1/docs/query-guide/#source">Source</a>)*<br> <div style="padding-left: 1em;"><p><p style="word-wrap: break-word;margin: 0;">The http-service source receives POST requests via HTTP and HTTPS protocols in format such as <code>text</code>, <code>XML</code> and <code>JSON</code> and sends responses via its corresponding http-service-response sink correlated through a unique <code>source.id</code>.<br>For request and response correlation, it generates a <code>messageId</code> upon each incoming request and expose it via transport properties in the format <code>trp:messageId</code> to correlate them with the responses at the http-service-response sink.<br>The request headers and properties can be accessed via transport properties in the format <code>trp:&lt;header&gt;</code>.<br>It also supports basic authentication to ensure events are received from authorized users/systems.</p></p></div>

## Dependencies 

There are no other dependencies needed for this extension. 

## Installation

For installing this extension on various siddhi execution environments refer Siddhi documentation section on <a target="_blank" href="https://siddhi.io/redirect/add-extensions.html">adding extensions</a>.

## Support and Contribution

* We encourage users to ask questions and get support via <a target="_blank" href="https://stackoverflow.com/questions/tagged/siddhi">StackOverflow</a>, make sure to add the `siddhi` tag to the issue for better response.

* If you find any issues related to the extension please report them on <a target="_blank" href="https://github.com/siddhi-io/siddhi-execution-string/issues">the issue tracker</a>.

* For production support and other contribution related information refer <a target="_blank" href="https://siddhi.io/community/">Siddhi Community</a> documentation.
