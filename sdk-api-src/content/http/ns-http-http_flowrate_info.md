---
UID: NS:http._HTTP_FLOWRATE_INFO
title: HTTP_FLOWRATE_INFO (http.h)
description: The transfer rate of a response.
helpviewer_keywords: ["*PHTTP_FLOWRATE_INFO","HTTP_FLOWRATE_INFO","HTTP_FLOWRATE_INFO structure [HTTP]","PHTTP_FLOWRATE_INFO","PHTTP_FLOWRATE_INFO structure pointer [HTTP]","http.http_flowrate_info","http/HTTP_FLOWRATE_INFO","http/PHTTP_FLOWRATE_INFO"]
old-location: http\http_flowrate_info.htm
tech.root: http
ms.assetid: 5b52ef5b-dc82-4a87-9204-d32134074c31
ms.date: 12/05/2018
ms.keywords: '*PHTTP_FLOWRATE_INFO, HTTP_FLOWRATE_INFO, HTTP_FLOWRATE_INFO structure [HTTP], PHTTP_FLOWRATE_INFO, PHTTP_FLOWRATE_INFO structure pointer [HTTP], http.http_flowrate_info, http/HTTP_FLOWRATE_INFO, http/PHTTP_FLOWRATE_INFO'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: HTTP_FLOWRATE_INFO, *PHTTP_FLOWRATE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_FLOWRATE_INFO
 - http/_HTTP_FLOWRATE_INFO
 - PHTTP_FLOWRATE_INFO
 - http/PHTTP_FLOWRATE_INFO
 - HTTP_FLOWRATE_INFO
 - http/HTTP_FLOWRATE_INFO
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
 - HTTP_FLOWRATE_INFO
---

# HTTP_FLOWRATE_INFO structure


## -description

The transfer rate of a response

## -struct-fields

### -field Flags

An <a href="/windows/desktop/api/http/ns-http-http_property_flags">HTTP_PROPERTY_FLAGS</a> structure specifying whether the property is present.

### -field MaxBandwidth

The maximum bandwidth represented in bytes/second.  This is the maximum bandwidth for the response after the burst content, whose size is specified in <b>BurstSize</b>,  has been sent.

### -field MaxPeakBandwidth

The peak bandwidth represented in bytes/second.  This is the maximum bandwidth at which the burst is delivered.

### -field BurstSize

The size of the content, in bytes, to be delivered at <b>MaxPeakBandwidth</b>.  Once this content has been delivered, the response is throttled at <b>MaxBandwidth</b>.  If the HTTP Server application sends responses at a rate slower than <b>MaxBandwidth</b>, the response is subject to burst again at <b>MaxPeakBandwidth</b> to maximize bandwidth utilization.

## -remarks

This structure allows an HTTP Server application to maximize the network bandwidth use by throttling down the transfer rate of an HTTP response.  This is especially useful in serving media content where the initial burst of the content is served at a higher transfer rate and then throttled.  This allows content from a larger number of media to be served concurrently.

The transfer rate is allowed to exceed <b> MaxBandwidth</b> in two cases:<ul>
<li>If the connection slows and the transfer rate falls below <b> MaxBandwidth</b>, the application can go beyond <b> MaxBandwidth</b> to catch up.</li>
<li>The beginning of a response is allowed to exceed <b> MaxBandwidth</b>.  For example, a server may  transfer media file at high speed at the beginning in order to expedite playback on the client.
For example, if that client needs initial 20KB of the file to start playback, the server might have this variable set to 20KB.
</li>
</ul>When <b> MaxBandwidth</b> is exceeded, <b> MaxPeakBandwidth </b> is still the absolute upper limit.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>