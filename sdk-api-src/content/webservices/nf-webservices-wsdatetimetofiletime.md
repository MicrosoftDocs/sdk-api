---
UID: NF:webservices.WsDateTimeToFileTime
title: WsDateTimeToFileTime function (webservices.h)
description: Converts a WS_DATETIME object into a FILETIME object. A reference to the FILETIME object is returned by output parameter.
helpviewer_keywords: ["WsDateTimeToFileTime","WsDateTimeToFileTime function [Web Services for Windows]","webservices/WsDateTimeToFileTime","wsw.wsdatetimetofiletime"]
old-location: wsw\wsdatetimetofiletime.htm
tech.root: wsw
ms.assetid: 19e987d8-fe20-4bc6-a887-77bc1cfa65cf
ms.date: 12/05/2018
ms.keywords: WsDateTimeToFileTime, WsDateTimeToFileTime function [Web Services for Windows], webservices/WsDateTimeToFileTime, wsw.wsdatetimetofiletime
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
 - WsDateTimeToFileTime
 - webservices/WsDateTimeToFileTime
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
 - WsDateTimeToFileTime
---

# WsDateTimeToFileTime function


## -description

Converts a <a href="/windows/desktop/api/webservices/ns-webservices-ws_datetime">WS_DATETIME</a> object into a FILETIME object.
       A reference to the FILETIME object is returned by output parameter.

## -parameters

### -param dateTime [in]

A pointer to the <a href="/windows/desktop/api/webservices/ns-webservices-ws_datetime">WS_DATETIME</a> structure to convert.

### -param fileTime [out]

A pointer to the new FILETIME object that contains the converted time.

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

A FILETIME cannot represent dates between January 1, 0001 and January 1, 1601.  A <a href="/windows/desktop/api/webservices/ns-webservices-ws_datetime">WS_DATETIME</a> within this range causes the function to return <b>WS_E_INVALID_FORMAT</b>.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)