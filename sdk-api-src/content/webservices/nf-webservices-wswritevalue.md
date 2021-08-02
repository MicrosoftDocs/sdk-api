---
UID: NF:webservices.WsWriteValue
title: WsWriteValue function (webservices.h)
description: This operation derives the best representation for a primitive value from the underlying encoding and passes the derived value to a Writer object.
helpviewer_keywords: ["WsWriteValue","WsWriteValue function [Web Services for Windows]","webservices/WsWriteValue","wsw.wswritevalue"]
old-location: wsw\wswritevalue.htm
tech.root: wsw
ms.assetid: c7b9d014-89b5-4959-b49e-ee2cdeb41f7c
ms.date: 12/05/2018
ms.keywords: WsWriteValue, WsWriteValue function [Web Services for Windows], webservices/WsWriteValue, wsw.wswritevalue
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
 - WsWriteValue
 - webservices/WsWriteValue
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
 - WsWriteValue
---

# WsWriteValue function


## -description

This operation derives the best representation for a  primitive value from the underlying encoding and passes the derived value to a Writer object.
      <div class="alert"><b>Note</b>  It is generally more efficient to use this function to write out primitive values rather than converting
        the value to text and subsequently using <a href="/windows/desktop/api/webservices/nf-webservices-wswritechars">WsWriteChars</a>.</div>
<div> </div>

## -parameters

### -param writer [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object to which the value is written.  The pointer must reference a valid <b>XML Writer</b> object.

### -param valueType [in]

Indicates the Type of primitive value referenced by the <i>value</i> parameter.

I

### -param value

A void  pointer to the primitive value.

### -param valueSize [in]

The size in bytes of the value being written.

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

<b>WsWriteValue</b> may be called only once between <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartattribute">WsWriteStartAttribute</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wswriteendattribute">WsWriteEndAttribute</a>.
        It may not be combined with <a href="/windows/desktop/api/webservices/nf-webservices-wswritechars">WsWriteChars</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wswritebytes">WsWriteBytes</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wswritecharsutf8">WsWriteCharsUtf8</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wswritetext">WsWriteText</a> when writing an attribute.