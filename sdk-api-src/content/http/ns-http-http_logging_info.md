---
UID: NS:http._HTTP_LOGGING_INFO
title: HTTP_LOGGING_INFO (http.h)
description: Used to enable server side logging on a URL Group or on a server session.
helpviewer_keywords: ["*PHTTP_LOGGING_INFO","*PHTTP_LOGGING_INFO structure [HTTP]","HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER","HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY","HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY","HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION","HTTP_LOGGING_INFO","HTTP_LOGGING_INFO structure [HTTP]","HttpLoggingRolloverDaily","HttpLoggingRolloverHourly","HttpLoggingRolloverMonthly","HttpLoggingRolloverSize","HttpLoggingRolloverWeekly","HttpLoggingTypeIIS","HttpLoggingTypeNCSA","HttpLoggingTypeRaw","HttpLoggingTypeW3C","http.http_logging_info","http/*PHTTP_LOGGING_INFO","http/HTTP_LOGGING_INFO"]
old-location: http\http_logging_info.htm
tech.root: http
ms.assetid: 12e12f83-c36a-4b4e-8890-50566cf00c2b
ms.date: 12/05/2018
ms.keywords: '*PHTTP_LOGGING_INFO, *PHTTP_LOGGING_INFO structure [HTTP], HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER, HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY, HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY, HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION, HTTP_LOGGING_INFO, HTTP_LOGGING_INFO structure [HTTP], HttpLoggingRolloverDaily, HttpLoggingRolloverHourly, HttpLoggingRolloverMonthly, HttpLoggingRolloverSize, HttpLoggingRolloverWeekly, HttpLoggingTypeIIS, HttpLoggingTypeNCSA, HttpLoggingTypeRaw, HttpLoggingTypeW3C, http.http_logging_info, http/*PHTTP_LOGGING_INFO, http/HTTP_LOGGING_INFO'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HTTP_LOGGING_INFO, *PHTTP_LOGGING_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_LOGGING_INFO
 - http/_HTTP_LOGGING_INFO
 - PHTTP_LOGGING_INFO
 - http/PHTTP_LOGGING_INFO
 - HTTP_LOGGING_INFO
 - http/HTTP_LOGGING_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_LOGGING_INFO
---

# HTTP_LOGGING_INFO structure


## -description

The <b>HTTP_LOGGING_INFO</b> structure is used to enable server side logging on a URL Group or on a server session.

This structure must be used when setting or querying  the <a href="/windows/desktop/api/http/ne-http-http_server_property">HttpServerLoggingProperty</a> on a URL Group or server session.

## -struct-fields

### -field Flags

The <a href="/windows/desktop/api/http/ns-http-http_property_flags">HTTP_PROPERTY_FLAGS</a> structure that specifies whether the property is present.

### -field LoggingFlags

The optional logging flags change the default logging behavior.

These  can be one or more of the following <a href="/windows/desktop/Http/http-logging-flag--constants">HTTP_LOGGING_FLAG</a> values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></a><a id="http_logging_flag_local_time_rollover"></a><dl>
<dt><b>HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER</b></dt>
</dl>
</td>
<td width="60%">
Changes the log file rollover time to local time. By default log file rollovers are based on GMT.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></a><a id="http_logging_flag_use_utf8_conversion"></a><dl>
<dt><b>HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION</b></dt>
</dl>
</td>
<td width="60%">
By default, the unicode logging fields are converted to multibytes using the systems local code page. If this flags is set, the UTF8 conversion is used instead.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></a><a id="http_logging_flag_log_errors_only"></a><dl>
<dt><b>HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The log errors only flag enables logging errors only. By default, both error and success request are logged.

The <b>HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY</b> and <b>HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY</b> flags are used to perform selective logging. Only one of these flags can be set at a time; they are mutually exclusive.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></a><a id="http_logging_flag_log_success_only"></a><dl>
<dt><b>HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The log success only flag enables logging successful requests only. By default, both error and success request are logged.

The <b>HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY</b>  and <b>HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY</b> flags are used to perform selective logging. Only one of these flags can be set at a time; they are mutually exclusive.

</td>
</tr>
</table>

### -field SoftwareName

The optional software name string used in W3C type logging. This name is not used for other types of logging. If this parameter is <b>NULL</b>, the HTTP Server API logs a default string.

### -field SoftwareNameLength

The length, in bytes, of the software name. The length cannot be greater than <b>MAX_PATH</b>.

If the <b>SoftwareName</b> member is <b>NULL</b>, this length must be zero.

### -field DirectoryNameLength

The length, in bytes, of the directory name. The length cannot be greater than 424  bytes.

### -field DirectoryName

The logging directory under which the log files are created. The directory string must be a fully qualified path including the drive letter.

  Applications can use a UNC path to a remote machine to enable UNC logging.

### -field Format

A member of the <a href="/windows/desktop/api/http/ne-http-http_logging_type">HTTP_LOGGING_TYPE</a> enumeration specifying one of the following log file formats.

<table>
<tr>
<th>Format</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpLoggingTypeW3C"></a><a id="httploggingtypew3c"></a><a id="HTTPLOGGINGTYPEW3C"></a><dl>
<dt><b>HttpLoggingTypeW3C</b></dt>
</dl>
</td>
<td width="60%">
The log format is W3C style extended logging. With this format, application can pick a combination of log fields to be logged. When W3C logging is set on a URL group, logging is similar to the IIS6 site logging. When W3C logging is set on a server session, this logging functions as a centralized logging for all of the URL Groups.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpLoggingTypeIIS"></a><a id="httploggingtypeiis"></a><a id="HTTPLOGGINGTYPEIIS"></a><dl>
<dt><b>HttpLoggingTypeIIS</b></dt>
</dl>
</td>
<td width="60%">
The log format is IIS6/5 style logging. This format has fixed field definitions; applications cannot select the fields that are logged. This format cannot be used for logging a server session.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpLoggingTypeNCSA"></a><a id="httploggingtypencsa"></a><a id="HTTPLOGGINGTYPENCSA"></a><dl>
<dt><b>HttpLoggingTypeNCSA</b></dt>
</dl>
</td>
<td width="60%">
 The log format is NCSA style logging. This format has fixed field definitions; applications cannot select the fields that are logged. This format cannot be used for logging a server session.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpLoggingTypeRaw"></a><a id="httploggingtyperaw"></a><a id="HTTPLOGGINGTYPERAW"></a><dl>
<dt><b>HttpLoggingTypeRaw</b></dt>
</dl>
</td>
<td width="60%">
The log format is centralized binary logging. This format has fixed field definitions; applications cannot select the fields that are logged. This format cannot be used for logging a URL Group.

</td>
</tr>
</table>

### -field Fields

The fields that are logged when the format is set to W3C. These  can be one or more of the <a href="/windows/desktop/Http/http-log-field--constants">HTTP_LOG_FIELD_ Constants</a> values.

When the logging format is W3C is , applications must specify the log fields otherwise no fields are logged.

### -field pExtFields

Reserved. Set to 0 (zero) or <b>NULL</b>.

### -field NumOfExtFields

Reserved. Set to 0 (zero) or <b>NULL</b>.

### -field MaxRecordSize

Reserved. Set to 0 (zero) or <b>NULL</b>.

### -field RolloverType

One of the following members of the <a href="/windows/desktop/api/http/ne-http-http_logging_rollover_type">HTTP_LOGGING_ROLLOVER_TYPE</a> enumeration specifying the criteria for log file rollover.

<table>
<tr>
<th>Rollover Type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpLoggingRolloverSize"></a><a id="httploggingrolloversize"></a><a id="HTTPLOGGINGROLLOVERSIZE"></a><dl>
<dt><b>HttpLoggingRolloverSize</b></dt>
</dl>
</td>
<td width="60%">
The log files are rolled over when they reach or exceed a specified size.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpLoggingRolloverDaily"></a><a id="httploggingrolloverdaily"></a><a id="HTTPLOGGINGROLLOVERDAILY"></a><dl>
<dt><b>HttpLoggingRolloverDaily</b></dt>
</dl>
</td>
<td width="60%">
The log files are rolled over every day.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpLoggingRolloverWeekly"></a><a id="httploggingrolloverweekly"></a><a id="HTTPLOGGINGROLLOVERWEEKLY"></a><dl>
<dt><b>HttpLoggingRolloverWeekly</b></dt>
</dl>
</td>
<td width="60%">
The log files are rolled over every week.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpLoggingRolloverMonthly"></a><a id="httploggingrollovermonthly"></a><a id="HTTPLOGGINGROLLOVERMONTHLY"></a><dl>
<dt><b>HttpLoggingRolloverMonthly</b></dt>
</dl>
</td>
<td width="60%">
The log files are rolled over every month.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpLoggingRolloverHourly"></a><a id="httploggingrolloverhourly"></a><a id="HTTPLOGGINGROLLOVERHOURLY"></a><dl>
<dt><b>HttpLoggingRolloverHourly</b></dt>
</dl>
</td>
<td width="60%">
The log files are rolled over every hour.

</td>
</tr>
</table>

### -field RolloverSize

The maximum size, in bytes, after which the log files is rolled over. A value of <b>HTTP_LIMIT_INFINITE</b> indicates an unlimited size. The minimum value cannot be smaller than <b>HTTP_MIN_ALLOWED_LOG_FILE_ROLLOVER_SIZE</b> (1024 * 1024).

This field is used only for <b>HttpLoggingRolloverSize</b> rollover type and should be set to zero for all other types.

When rollover type is <b>HttpLoggingRolloverSize</b>, applications must specify the maximum size for the log file.

### -field pSecurityDescriptor

The security descriptor that is applied to the log files directory and all sub-directories. If this member is <b>NULL</b>, either the system default ACL is used or the ACL is inherited from the parent directory.

## -remarks

The <a href="/windows/desktop/api/http/ne-http-http_server_property">HttpServerLoggingProperty</a> property sets one of four types of server side logging: HttpLoggingTypeW3C, HttpLoggingTypeIIS, HttpLoggingTypeNCSA, or HttpLoggingTypeRaw. When this property is set on a server session it functions as centralized form of logging for all of the URL groups under that server session. Requests that are routed to one of the URL groups under the server session are logged in one centralized log file. The configuration parameters for the log file are passed in the  <b>HTTP_LOGGING_INFO</b> structure in the call to   <a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>.

When this property is set on a URL Group, logging is performed only on  requests that are routed to the URL Group. 
Log files are created when the request arrives on the URL Group or server session, they are not created when logging is configured.

Applications must ensure that the directory specified in the <b>DirectoryName</b> member is unique.  

The log files names are based on the specified rollover type. The following table shows the naming conventions for log files.
<table>
<tr>
<th>Format</th>
<th>Rollover  type </th>
<th>File name pattern</th>
</tr>
<tr>
<td>Microsoft IIS Log Format</td>
<td>Size</td>
<td>inetsvnn.log</td>
</tr>
<tr>
<td></td>
<td>Hourly</td>
<td>inyymmddhh.log</td>
</tr>
<tr>
<td></td>
<td>Daily</td>
<td>inyymmdd.log</td>
</tr>
<tr>
<td></td>
<td>Weekly</td>
<td>inyymmww.log</td>
</tr>
<tr>
<td></td>
<td>Monthly</td>
<td>inyymm.log</td>
</tr>
<tr>
<td>NCSA Common Log File Format</td>
<td>Size</td>
<td>ncsann.log
</td>
</tr>
<tr>
<td></td>
<td>Hourly</td>
<td>ncyymmddhh.log</td>
</tr>
<tr>
<td></td>
<td>Daily</td>
<td>ncyymmdd.log</td>
</tr>
<tr>
<td></td>
<td>Weekly</td>
<td>ncyymmww.log</td>
</tr>
<tr>
<td></td>
<td>Monthly</td>
<td>ncyymm.log</td>
</tr>
<tr>
<td>W3C Extended Log File Format</td>
<td>Size</td>
<td>extendnn.log</td>
</tr>
<tr>
<td></td>
<td>Hourly</td>
<td>exyymmddhh.log</td>
</tr>
<tr>
<td></td>
<td>Daily</td>
<td>exyymmdd.log</td>
</tr>
<tr>
<td></td>
<td>Weekly</td>
<td>exyymmww.log</td>
</tr>
<tr>
<td></td>
<td>Monthly</td>
<td>exyymm.log</td>
</tr>
</table>
 



The letters yy, mm, ww, dd, hh, and nn in the table represent the following digits:<ul>
<li>yy: The two digit representation of the year.</li>
<li>mm: The two digit representation of the month.</li>
<li>ww: The two digit representation of the week.</li>
<li>dd: The two digit representation of the day.</li>
<li>hh: The two digit representation of the hour in 24 hour notation.</li>
<li>nn: The two digit representation of the numerical sequence.</li>
</ul>


Please note that in the HTTP version 2.0 API, the <a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a> and <a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a> have been revisioned to allow applications to pass an <a href="/windows/desktop/api/http/ns-http-http_log_fields_data">HTTP_LOG_FIELDS_DATA</a> structure so the response can be logged. Setting the <b>HttpServerLoggingProperty</b>  property on a server session or a URL group does not mean that HTTP responses are logged. Logging on the URL group or the server session will not take place unless the calls to <b>HttpSendResponseEntityBody</b> and <b>HttpSendHttpResponse</b> include an optional <b>HTTP_LOG_FIELDS_DATA</b> structure. For more information, see the <b>HTTP_LOG_FIELDS_DATA</b> topic.

For information on the log file formats, see the <a href="/previous-versions/iis/6.0-sdk/ms525807(v=vs.90)">IIS Log File Formats</a> topic.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/Http/http-logging-flag--constants">HTTP_LOGGING_FLAG_ Constants</a>



<a href="/windows/desktop/api/http/ne-http-http_logging_rollover_type">HTTP_LOGGING_ROLLOVER_TYPE</a>



<a href="/windows/desktop/api/http/ne-http-http_logging_type">HTTP_LOGGING_TYPE</a>



<a href="/windows/desktop/Http/http-log-field--constants">HTTP_LOG_FIELD_ Constants</a>



<a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a>



<a href="/windows/desktop/api/http/nf-http-httpcloserequestqueue">HttpCloseRequestQueue</a>



<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a>



<a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpshutdownrequestqueue">HttpShutdownRequestQueue</a>