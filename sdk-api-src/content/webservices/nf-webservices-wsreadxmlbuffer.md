---
UID: NF:webservices.WsReadXmlBuffer
title: WsReadXmlBuffer function (webservices.h)
description: Reads the current node from a reader into a WS_XML_BUFFER.
helpviewer_keywords: ["WsReadXmlBuffer","WsReadXmlBuffer function [Web Services for Windows]","webservices/WsReadXmlBuffer","wsw.wsreadxmlbuffer"]
old-location: wsw\wsreadxmlbuffer.htm
tech.root: wsw
ms.assetid: d8d849b7-6acf-4007-a904-144200c934f6
ms.date: 12/05/2018
ms.keywords: WsReadXmlBuffer, WsReadXmlBuffer function [Web Services for Windows], webservices/WsReadXmlBuffer, wsw.wsreadxmlbuffer
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
 - WsReadXmlBuffer
 - webservices/WsReadXmlBuffer
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
 - WsReadXmlBuffer
---

# WsReadXmlBuffer function


## -description

Reads the current node from a reader into a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a>.

## -parameters

### -param reader [in]

The reader from which to read into the XML buffer.

### -param heap [in]

The heap from which to allocate the XML buffer.

### -param xmlBuffer

The XML buffer is returned here.

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

If the reader must be positioned at either <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_node_type">WS_XML_NODE_TYPE_BOF</a>, or <b>WS_XML_NODE_TYPE_ELEMENT</b>.
      

If the reader is positioned at <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_node_type">WS_XML_NODE_TYPE_BOF</a>, then the entire document will be copied from the
        reader into the XML buffer.
      

If the reader is positioned at <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_node_type">WS_XML_NODE_TYPE_ELEMENT</a>, then the element and all its children will be
        read into the XML buffer.