---
UID: NF:webservices.WsWriteBytes
title: WsWriteBytes function (webservices.h)
description: Writes bytes to the writer in a format optimized for the encoding. When writing in a text encoding, it will emit the bytes encoded in base64. When writing to a binary format, it will emit the bytes directly.
helpviewer_keywords: ["WsWriteBytes","WsWriteBytes function [Web Services for Windows]","webservices/WsWriteBytes","wsw.wswritebytes"]
old-location: wsw\wswritebytes.htm
tech.root: wsw
ms.assetid: 1fa9ecfc-c791-459f-ae11-ffcdc82b7145
ms.date: 12/05/2018
ms.keywords: WsWriteBytes, WsWriteBytes function [Web Services for Windows], webservices/WsWriteBytes, wsw.wswritebytes
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
 - WsWriteBytes
 - webservices/WsWriteBytes
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
 - WsWriteBytes
---

# WsWriteBytes function


## -description

Writes bytes to the writer in a format optimized for the encoding.  When writing
         in a text encoding, it will emit the bytes encoded in base64.  When writing to 
         a binary format, it will emit the bytes directly.

## -parameters

### -param writer [in]

The writer to which the bytes will be written.

### -param bytes

The bytes to write to the document.

### -param byteCount [in]

The number bytes to write to the document.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

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

<b>WsWriteBytes</b> may be called more than once between <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartattribute">WsWriteStartAttribute</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wswriteendattribute">WsWriteEndAttribute</a>.  It may
        not be combined with <a href="/windows/desktop/api/webservices/nf-webservices-wswritechars">WsWriteChars</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wswritecharsutf8">WsWriteCharsUtf8</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wswritevalue">WsWriteValue</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wswritetext">WsWriteText</a> when writing an attribute.
      

For the <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_mtom_encoding">WS_XML_WRITER_MTOM_ENCODING</a>, if the byteCount exceeds the maxInlineByteCount specified
        during <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutput">WsSetOutput</a> then the bytes will be buffered and  placed in their own MIME part.  Otherwise
        the bytes are encoded in base64 and placed directly in the document.
      

For the <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_mtom_encoding">WS_XML_WRITER_MTOM_ENCODING</a>, if the element containing the bytes has an attribute with
        the name 'contentType' and the namespace 'http://www.w3.org/2004/11/xmlmime', then the value of the attribute
        will be reflected in the content type header for the MIME part as described in 
        XML-binary Optimized Packaging.