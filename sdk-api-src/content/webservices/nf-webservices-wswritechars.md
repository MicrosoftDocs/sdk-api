---
UID: NF:webservices.WsWriteChars
title: WsWriteChars function (webservices.h)
description: Writes a series of characters to an element or attribute.
helpviewer_keywords: ["WsWriteChars","WsWriteChars function [Web Services for Windows]","webservices/WsWriteChars","wsw.wswritechars"]
old-location: wsw\wswritechars.htm
tech.root: wsw
ms.assetid: e435058f-62b5-4ae9-800e-e022033a9664
ms.date: 12/05/2018
ms.keywords: WsWriteChars, WsWriteChars function [Web Services for Windows], webservices/WsWriteChars, wsw.wswritechars
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
 - WsWriteChars
 - webservices/WsWriteChars
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
 - WsWriteChars
---

# WsWriteChars function


## -description

Writes a series of characters to an element or attribute.
      
To write characters to an attribute value, call <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartattribute">WsWriteStartAttribute</a> first. Only whitespace characters may be written at the root of an xml document unless the <b>WS_XML_WRITER_PROPERTY_ALLOW_FRAGMENT</b> has been set to <b>TRUE</b>.

## -parameters

### -param writer [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object to which the characters are written.  The pointer must reference a valid <b>XML Writer</b> object.

### -param chars

A pointer to the characters to write.

### -param charCount [in]

The number of characters to write.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>

## -remarks

<b>WsWriteChars</b> can be called more than once between <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartattribute">WsWriteStartAttribute</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wswriteendattribute">WsWriteEndAttribute</a>.  It cannot be combined with <a href="/windows/desktop/api/webservices/nf-webservices-wswritecharsutf8">WsWriteCharsUtf8</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wswritebytes">WsWriteBytes</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wswritevalue">WsWriteValue</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wswritetext">WsWriteText</a> when writing an attribute.