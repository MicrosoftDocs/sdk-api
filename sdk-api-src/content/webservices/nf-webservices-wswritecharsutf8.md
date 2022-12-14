---
UID: NF:webservices.WsWriteCharsUtf8
title: WsWriteCharsUtf8 function (webservices.h)
description: Writes a series of characters encoded as UTF-8 to an element or attribute.
helpviewer_keywords: ["WsWriteCharsUtf8","WsWriteCharsUtf8 function [Web Services for Windows]","webservices/WsWriteCharsUtf8","wsw.wswritecharsutf8"]
old-location: wsw\wswritecharsutf8.htm
tech.root: wsw
ms.assetid: 53cdaf22-21ed-4e5a-8034-d5a4725b9da3
ms.date: 12/05/2018
ms.keywords: WsWriteCharsUtf8, WsWriteCharsUtf8 function [Web Services for Windows], webservices/WsWriteCharsUtf8, wsw.wswritecharsutf8
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
 - WsWriteCharsUtf8
 - webservices/WsWriteCharsUtf8
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
 - WsWriteCharsUtf8
---

# WsWriteCharsUtf8 function


## -description

Writes a series of characters encoded as UTF-8 to an element or attribute.
      To write characters to an attribute value, call <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartattribute">WsWriteStartAttribute</a> first.
      Only whitespace characters may be written at the root of an xml document unless the
        <b>WS_XML_WRITER_PROPERTY_ALLOW_FRAGMENT</b> has been set to <b>TRUE</b>.

## -parameters

### -param writer [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object to which the characters are written.  The pointer must reference a valid <b>XML Writer</b> object.

### -param bytes

A pointer to the encoded UTF-8 characters to write.

### -param byteCount [in]

The number of bytes to write.

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

<b>WsWriteCharsUtf8</b> can be called more than once between <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartattribute">WsWriteStartAttribute</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wswriteendattribute">WsWriteEndAttribute</a>.  It cannot be combined with <a href="/windows/desktop/api/webservices/nf-webservices-wswritechars">WsWriteChars</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wswritebytes">WsWriteBytes</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wswritevalue">WsWriteValue</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wswritetext">WsWriteText</a> when writing an attribute.