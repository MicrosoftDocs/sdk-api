---
UID: NE:http._HTTP_LOGGING_ROLLOVER_TYPE
title: HTTP_LOGGING_ROLLOVER_TYPE (http.h)
description: Defines the log file rollover types.
helpviewer_keywords: ["*PHTTP_LOGGING_ROLLOVER_TYPE","*PHTTP_LOGGING_ROLLOVER_TYPE enumeration [HTTP]","HTTP_LOGGING_ROLLOVER_TYPE","HTTP_LOGGING_ROLLOVER_TYPE enumeration [HTTP]","HttpLoggingRolloverDaily","HttpLoggingRolloverHourly","HttpLoggingRolloverMonthly","HttpLoggingRolloverSize","HttpLoggingRolloverWeekly","http.http_logging_rollover_type","http/*PHTTP_LOGGING_ROLLOVER_TYPE","http/HTTP_LOGGING_ROLLOVER_TYPE","http/HttpLoggingRolloverDaily","http/HttpLoggingRolloverHourly","http/HttpLoggingRolloverMonthly","http/HttpLoggingRolloverSize","http/HttpLoggingRolloverWeekly"]
old-location: http\http_logging_rollover_type.htm
tech.root: http
ms.assetid: f1560f05-f7c4-46f1-ad9e-d737d0019b41
ms.date: 12/05/2018
ms.keywords: '*PHTTP_LOGGING_ROLLOVER_TYPE, *PHTTP_LOGGING_ROLLOVER_TYPE enumeration [HTTP], HTTP_LOGGING_ROLLOVER_TYPE, HTTP_LOGGING_ROLLOVER_TYPE enumeration [HTTP], HttpLoggingRolloverDaily, HttpLoggingRolloverHourly, HttpLoggingRolloverMonthly, HttpLoggingRolloverSize, HttpLoggingRolloverWeekly, http.http_logging_rollover_type, http/*PHTTP_LOGGING_ROLLOVER_TYPE, http/HTTP_LOGGING_ROLLOVER_TYPE, http/HttpLoggingRolloverDaily, http/HttpLoggingRolloverHourly, http/HttpLoggingRolloverMonthly, http/HttpLoggingRolloverSize, http/HttpLoggingRolloverWeekly'
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
req.typenames: HTTP_LOGGING_ROLLOVER_TYPE, *PHTTP_LOGGING_ROLLOVER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_LOGGING_ROLLOVER_TYPE
 - http/_HTTP_LOGGING_ROLLOVER_TYPE
 - PHTTP_LOGGING_ROLLOVER_TYPE
 - http/PHTTP_LOGGING_ROLLOVER_TYPE
 - HTTP_LOGGING_ROLLOVER_TYPE
 - http/HTTP_LOGGING_ROLLOVER_TYPE
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
 - HTTP_LOGGING_ROLLOVER_TYPE
---

# HTTP_LOGGING_ROLLOVER_TYPE enumeration


## -description

The <b>HTTP_LOGGING_ROLLOVER_TYPE</b> enumeration defines the log file rollover types.

This enumeration is used  in the <a href="/windows/desktop/api/http/ns-http-http_logging_info">HTTP_LOGGING_INFO</a> structure.

## -enum-fields

### -field HttpLoggingRolloverSize

The log files are rolled over when they reach a specified size.

### -field HttpLoggingRolloverDaily

The log files are rolled over every day.

### -field HttpLoggingRolloverWeekly

The log files are rolled over every week.

### -field HttpLoggingRolloverMonthly

The log files are rolled over every month.

### -field HttpLoggingRolloverHourly

The log files are rolled over every hour, based on GMT.

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

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="/windows/desktop/api/http/ns-http-http_logging_info">HTTP_LOGGING_INFO</a>