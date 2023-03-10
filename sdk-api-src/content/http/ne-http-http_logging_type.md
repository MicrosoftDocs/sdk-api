---
UID: NE:http._HTTP_LOGGING_TYPE
title: HTTP_LOGGING_TYPE (http.h)
description: Defines the type of logging that is performed.
helpviewer_keywords: ["*PHTTP_LOGGING_TYPE","*PHTTP_LOGGING_TYPE enumeration [HTTP]","HTTP_LOGGING_TYPE","HTTP_LOGGING_TYPE enumeration [HTTP]","HttpLoggingTypeIIS","HttpLoggingTypeNCSA","HttpLoggingTypeRaw","HttpLoggingTypeW3C","http.http_logging_type","http/*PHTTP_LOGGING_TYPE","http/HTTP_LOGGING_TYPE","http/HttpLoggingTypeIIS","http/HttpLoggingTypeNCSA","http/HttpLoggingTypeRaw","http/HttpLoggingTypeW3C"]
old-location: http\http_logging_type.htm
tech.root: http
ms.assetid: 74a32957-7305-4f2b-a509-7d6aa11d2052
ms.date: 12/05/2018
ms.keywords: '*PHTTP_LOGGING_TYPE, *PHTTP_LOGGING_TYPE enumeration [HTTP], HTTP_LOGGING_TYPE, HTTP_LOGGING_TYPE enumeration [HTTP], HttpLoggingTypeIIS, HttpLoggingTypeNCSA, HttpLoggingTypeRaw, HttpLoggingTypeW3C, http.http_logging_type, http/*PHTTP_LOGGING_TYPE, http/HTTP_LOGGING_TYPE, http/HttpLoggingTypeIIS, http/HttpLoggingTypeNCSA, http/HttpLoggingTypeRaw, http/HttpLoggingTypeW3C'
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
req.typenames: HTTP_LOGGING_TYPE, *PHTTP_LOGGING_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_LOGGING_TYPE
 - http/_HTTP_LOGGING_TYPE
 - PHTTP_LOGGING_TYPE
 - http/PHTTP_LOGGING_TYPE
 - HTTP_LOGGING_TYPE
 - http/HTTP_LOGGING_TYPE
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
 - HTTP_LOGGING_TYPE
---

# HTTP_LOGGING_TYPE enumeration


## -description

The <b>HTTP_LOGGING_TYPE</b> enumeration defines the type of logging that is performed.

This enumeration is used  in the <a href="/windows/desktop/api/http/ns-http-http_logging_info">HTTP_LOGGING_INFO</a> structure.

## -enum-fields

### -field HttpLoggingTypeW3C

The log format is W3C style extended logging. Applications choose the fields that are logged in the  <b>Fields</b> member of the <a href="/windows/desktop/api/http/ns-http-http_logging_info">HTTP_LOGGING_INFO</a> structure.

 When this type of logging is set on a URL Group, logging is similar to the IIS6 site logging. When set on a server session this format functions as a centralized logging for all of the URL Groups.

### -field HttpLoggingTypeIIS

The log format is IIS5/6 style logging. This format has a fixed field definition; applications cannot choose which fields are logged. This format cannot be chosen when setting the logging property on a server session.

### -field HttpLoggingTypeNCSA

The log format is NCSA style logging. This format has a fixed field definition; applications cannot choose which fields are logged. This format cannot be chosen when setting the logging property on a server session.

### -field HttpLoggingTypeRaw

The log format is centralized binary logging. This format has a fixed field definition; applications cannot choose which fields are logged. This format cannot be chosen when setting the logging property on a URL Group.

## -remarks

The log files are named based on the rollover type and logging format as shown in  the following table.


<table>
<tr>
<th>Format</th>
<th>Rollover  Type </th>
<th>Filename Pattern</th>
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
<td>inymmww.log</td>
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
 



The following table lists time element characters and what they represent. <table>
<tr>
<th>Item</th>
<th>Description </th>
</tr>
<tr>
<td>yy</td>
<td>The two digit representation of the year.</td>
</tr>
<tr>
<td>mm</td>
<td>The two digit representation of the month.</td>
</tr>
<tr>
<td>ww</td>
<td>The two digit representation of the week.</td>
</tr>
<tr>
<td>dd</td>
<td>The two digit representation of the day.</td>
</tr>
<tr>
<td>hh</td>
<td>The two digit representation of the hour in 24 hour notation.</td>
</tr>
<tr>
<td>nn</td>
<td>The two digit representation of the numerical sequence.</td>
</tr>
</table>
 



For more information about the log file formats, see <a href="/previous-versions/iis/6.0-sdk/ms525807(v=vs.90)">IIS Log File Formats</a>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="/windows/desktop/api/http/ns-http-http_logging_info">HTTP_LOGGING_INFO</a>