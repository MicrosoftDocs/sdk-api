---
UID: NF:webservices.WsFileTimeToDateTime
title: WsFileTimeToDateTime function (webservices.h)
description: Takes a reference to a FILETIME object and converts it into a WS_DATETIME object. A reference to the WS_DATETIME object is returned by output parameter.
helpviewer_keywords: ["WsFileTimeToDateTime","WsFileTimeToDateTime function [Web Services for Windows]","webservices/WsFileTimeToDateTime","wsw.wsfiletimetodatetime"]
old-location: wsw\wsfiletimetodatetime.htm
tech.root: wsw
ms.assetid: 75a547f8-c8dc-47c3-97c9-2a39b046263f
ms.date: 12/05/2018
ms.keywords: WsFileTimeToDateTime, WsFileTimeToDateTime function [Web Services for Windows], webservices/WsFileTimeToDateTime, wsw.wsfiletimetodatetime
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsFileTimeToDateTime
 - webservices/WsFileTimeToDateTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsFileTimeToDateTime
---

# WsFileTimeToDateTime function


## -description

Takes a reference to a FILETIME object and converts it into a <a href="/windows/desktop/api/webservices/ns-webservices-ws_datetime">WS_DATETIME</a> object.
       A reference to the WS_DATETIME object is returned by output parameter.

## -parameters

### -param fileTime [in]

A pointer to the FILETIME structure to convert.

### -param dateTime [out]

A pointer to the new WS_DATETIME object that has the newly converted time.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
</table>

## -remarks

A <a href="/windows/desktop/api/webservices/ns-webservices-ws_datetime">WS_DATETIME</a> cannot represent dates from the year 10000 and beyond.  A FILETIME representing a date
        later than this will cause the function return <b>WS_E_INVALID_FORMAT</b>.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

The format field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_datetime">WS_DATETIME</a> will be set to <a href="/windows/desktop/api/webservices/ne-webservices-ws_datetime_format">WS_DATETIME_FORMAT_UTC</a>.