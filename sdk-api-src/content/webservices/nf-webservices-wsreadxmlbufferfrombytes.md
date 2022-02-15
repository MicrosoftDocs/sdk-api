---
UID: NF:webservices.WsReadXmlBufferFromBytes
title: WsReadXmlBufferFromBytes function (webservices.h)
description: Uses a reader to convert a set of encoded bytes to a WS_XML_BUFFER.
helpviewer_keywords: ["WsReadXmlBufferFromBytes","WsReadXmlBufferFromBytes function [Web Services for Windows]","webservices/WsReadXmlBufferFromBytes","wsw.wsreadxmlbufferfrombytes"]
old-location: wsw\wsreadxmlbufferfrombytes.htm
tech.root: wsw
ms.assetid: 7ab68738-add0-4e2a-a036-5c6ecdd1f236
ms.date: 12/05/2018
ms.keywords: WsReadXmlBufferFromBytes, WsReadXmlBufferFromBytes function [Web Services for Windows], webservices/WsReadXmlBufferFromBytes, wsw.wsreadxmlbufferfrombytes
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
 - WsReadXmlBufferFromBytes
 - webservices/WsReadXmlBufferFromBytes
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
 - WsReadXmlBufferFromBytes
---

# WsReadXmlBufferFromBytes function


## -description

Uses a reader to convert a set of encoded bytes to a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a>.

## -parameters

### -param reader [in]

The reader to use to parse the encoded bytes.

### -param encoding [in, optional]

The encoding to use when parsing the bytes.  If <b>NULL</b>, a <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_reader_text_encoding">WS_XML_READER_TEXT_ENCODING</a> 
          with a charset of <a href="/windows/desktop/api/webservices/ne-webservices-ws_charset">WS_CHARSET_AUTO</a> will be used.

### -param properties

An array of optional properties of the reader.  See <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_property">WS_XML_READER_PROPERTY</a>.

### -param propertyCount [in]

The number of properties.

### -param bytes

The bytes to parse.

### -param byteCount [in]

The number of bytes to parse.

### -param heap [in]

The heap from which to allocate the XML buffer.

### -param xmlBuffer

The XML buffer into which the bytes were read is returned here.

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

The function will parse the entire contents according to the specified encoding and store it into a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a>.
      

The reader will be left in an undefined state after calling this function.  However, <b>WsReadXmlBufferFromBytes</b> may be used again with such a reader.  Otherwise, <a href="/windows/desktop/api/webservices/nf-webservices-wssetinput">WsSetInput</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wssetinputtobuffer">WsSetInputToBuffer</a> should be
        used to bring the reader back to a known state, or the reader should be freed using <a href="/windows/desktop/api/webservices/nf-webservices-wsfreereader">WsFreeReader</a>.