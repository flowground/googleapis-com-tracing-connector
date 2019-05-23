# ![LOGO](logo.png) Stackdriver Trace **flow**ground Connector

## Description

A generated **flow**ground connector for the Stackdriver Trace API (version v2).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/tracing/v2/swagger.json<br/>
Generated at: 2019-05-23T12:13:46+03:00

## API Description

Send and retrieve trace data from Stackdriver Trace. Data is generated and available by default for all App Engine applications. Data from other applications can be written to Stackdriver Trace for display, reporting, and analysis.


## Authorization

Supported authorization schemes:
- OAuth2
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Creates a new Span.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The resource name of the span in the following format:

    projects/[PROJECT_ID]traces/[TRACE_ID]/spans/SPAN_ID is a unique identifier for a trace within a project.
[SPAN_ID] is a unique identifier for a span within a trace,
assigned when the span is created.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `bearer_token` - _optional_ - OAuth bearer token.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `pp` - _optional_ - Pretty-print response.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Sends new spans to Stackdriver Trace or updates existing traces. If the<br/>
> name of a trace that you send matches that of an existing trace, new spans<br/>
> are added to the existing trace. Attempt to update existing spans results<br/>
> undefined behavior. If the name does not match, a new trace is created<br/>
> with given set of spans.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Required. Name of the project where the spans belong. The format is
`projects/PROJECT_ID`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `bearer_token` - _optional_ - OAuth bearer token.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `pp` - _optional_ - Pretty-print response.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns of a list of traces that match the specified filter conditions.

*Tags:* `projects`

#### Input Parameters
* `endTime` - _optional_ - Optional. Do not return traces whose start time is later than this time.
* `filter` - _optional_ - Opional. Return only traces that match this
[trace filter](/trace/docs/trace-filters). Example:

    "label:/http/url root:/_ah/background my_label:17"
* `orderBy` - _optional_ - Optional. A single field used to sort the returned traces.
Only the following field names can be used:

*   `trace_id`: the trace's ID field
*   `name`:  the root span's resource name
*   `duration`: the difference between the root span's start time and end time
*   `start`:  the start time of the root span

Sorting is in ascending order unless `desc` is appended to the sort field name.
Example: `"name desc"`).
* `pageSize` - _optional_ - Optional. The maximum number of results to return from this request.
Non-positive values are ignored. The presence of `next_page_token` in the
response indicates that more results might be available, even if fewer than
the maximum number of results is returned by this request.
* `pageToken` - _optional_ - Optional. If present, then retrieve the next batch of results from the
preceding call to this method.  `page_token` must be the value of
`next_page_token` from the previous response.  The values of other method
parameters should be identical to those in the previous call.
* `parent` - _required_ - Required. The project where the trace data is stored. The format
is `projects/PROJECT_ID`.
* `startTime` - _optional_ - Optional. Do not return traces whose end time is earlier than this time.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `pp` - _optional_ - Pretty-print response.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of spans within a trace.

*Tags:* `projects`

#### Input Parameters
* `pageToken` - _optional_ - Optional. If present, then retrieve the next batch of results from the
preceding call to this method. `page_token` must be the value of
`next_page_token` from the previous response. The values of other method
parameters should be identical to those in the previous call.
* `parent` - _required_ - Required: The resource name of the trace containing the spans to list.
The format is `projects/PROJECT_ID/traces/TRACE_ID`.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `bearer_token` - _optional_ - OAuth bearer token.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `pp` - _optional_ - Pretty-print response.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-tracing-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
