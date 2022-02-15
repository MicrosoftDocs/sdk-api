---
UID: NF:webservices.WsReadStartElement
title: WsReadStartElement function (webservices.h)
description: Calling this function advances the reader past a start element skipping any whitespace.
helpviewer_keywords: ["WsReadStartElement","WsReadStartElement function [Web Services for Windows]","webservices/WsReadStartElement","wsw.wsreadstartelement"]
old-location: wsw\wsreadstartelement.htm
tech.root: wsw
ms.assetid: 88661ae5-2112-4a41-8fcd-03c74f6ec170
ms.date: 12/05/2018
ms.keywords: WsReadStartElement, WsReadStartElement function [Web Services for Windows], webservices/WsReadStartElement, wsw.wsreadstartelement
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
 - WsReadStartElement
 - webservices/WsReadStartElement
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
 - WsReadStartElement
---

# WsReadStartElement function


## -description

Calling this function advances the reader past a start element skipping any whitespace.
      
After parsing if the Reader is not positioned on a start element it will return a <b>WS_E_INVALID_FORMAT</b> exception.

(See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

## -parameters

### -param reader [in]

A pointer to the <b>XML Reader</b> object used to read the Start element.

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
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
</table>

## -remarks

This function can fail for any of the reasons listed in <a href="/windows/desktop/api/webservices/nf-webservices-wsreadnode">WsReadNode</a>.