---
UID: NF:webservices.WsCreateXmlBuffer
title: WsCreateXmlBuffer function (webservices.h)
description: Creates an XML Buffer which can be used to process XML data .
helpviewer_keywords: ["WsCreateXmlBuffer","WsCreateXmlBuffer function [Web Services for Windows]","webservices/WsCreateXmlBuffer","wsw.wscreatexmlbuffer"]
old-location: wsw\wscreatexmlbuffer.htm
tech.root: wsw
ms.assetid: 4e122283-f285-4fff-b240-22e4a7476639
ms.date: 12/05/2018
ms.keywords: WsCreateXmlBuffer, WsCreateXmlBuffer function [Web Services for Windows], webservices/WsCreateXmlBuffer, wsw.wscreatexmlbuffer
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
 - WsCreateXmlBuffer
 - webservices/WsCreateXmlBuffer
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
 - WsCreateXmlBuffer
---

# WsCreateXmlBuffer function


## -description

Creates an <a href="/windows/desktop/wsw/xml-buffer">XML Buffer</a> which can be used to process XML data .

## -parameters

### -param heap [in]

Pointer to the <a href="/windows/desktop/wsw/ws-heap">WS_HEAP</a> structure representing the <a href="/windows/desktop/wsw/heap">heap</a> from which to allocate memory for the returned XML buffer.

### -param properties

An array of <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_buffer_property">WS_XML_BUFFER_PROPERTY</a> structures containing optional properties for the XML buffer.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param buffer

On   success, a pointer that receives the address of the  <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> structure representing the created XML buffer. The memory for this buffer is released when its heap is reset or released.
        

The XML buffer is initially  empty.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
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
</table>