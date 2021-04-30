---
UID: NF:webservices.WsSetWriterPosition
title: WsSetWriterPosition function (webservices.h)
description: Sets the current position of the writer. The position must have been obtained by a call to WsGetReaderPosition or WsGetWriterPosition.
helpviewer_keywords: ["WsSetWriterPosition","WsSetWriterPosition function [Web Services for Windows]","webservices/WsSetWriterPosition","wsw.wssetwriterposition"]
old-location: wsw\wssetwriterposition.htm
tech.root: wsw
ms.assetid: 1d23bda1-d1da-44d4-9a9d-258bba200b29
ms.date: 12/05/2018
ms.keywords: WsSetWriterPosition, WsSetWriterPosition function [Web Services for Windows], webservices/WsSetWriterPosition, wsw.wssetwriterposition
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
 - WsSetWriterPosition
 - webservices/WsSetWriterPosition
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
 - WsSetWriterPosition
---

# WsSetWriterPosition function


## -description

Sets the current position of the writer.  The position must have been obtained by a 
        call to <a href="/windows/desktop/api/webservices/nf-webservices-wsgetreaderposition">WsGetReaderPosition</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsgetwriterposition">WsGetWriterPosition</a>.

## -parameters

### -param writer [in]

The writer for which the current position will be set.

### -param nodePosition [in]

The position to set the writer to.

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
</table>

## -remarks

This can only be used on a writer that is set to an <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a>.
      

When writing to a buffer, the position represents the xml node before which new data will be placed.
      

See <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node_position">WS_XML_NODE_POSITION</a> for more information on using positions.