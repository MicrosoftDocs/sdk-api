---
UID: NF:webservices.WsWriteXmlBuffer
title: WsWriteXmlBuffer function (webservices.h)
description: Writes a WS_XML_BUFFER to a writer.
helpviewer_keywords: ["WsWriteXmlBuffer","WsWriteXmlBuffer function [Web Services for Windows]","webservices/WsWriteXmlBuffer","wsw.wswritexmlbuffer"]
old-location: wsw\wswritexmlbuffer.htm
tech.root: wsw
ms.assetid: a0845072-95dc-4d81-8322-514b8acff32a
ms.date: 12/05/2018
ms.keywords: WsWriteXmlBuffer, WsWriteXmlBuffer function [Web Services for Windows], webservices/WsWriteXmlBuffer, wsw.wswritexmlbuffer
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
 - WsWriteXmlBuffer
 - webservices/WsWriteXmlBuffer
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
 - WsWriteXmlBuffer
---

# WsWriteXmlBuffer function


## -description

Writes a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> to a writer.

## -parameters

### -param writer [in]

The writer to which the XML buffer will be written.

### -param xmlBuffer [in]

The XML buffer to write.

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

The function will copy the entire contents of the <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> to the writer at the current position.