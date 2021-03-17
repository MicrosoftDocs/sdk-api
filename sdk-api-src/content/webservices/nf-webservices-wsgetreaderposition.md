---
UID: NF:webservices.WsGetReaderPosition
title: WsGetReaderPosition function (webservices.h)
description: Returns the current position of the reader. This can only be used on a reader that is set to an XmlBuffer.
helpviewer_keywords: ["WsGetReaderPosition","WsGetReaderPosition function [Web Services for Windows]","webservices/WsGetReaderPosition","wsw.wsgetreaderposition"]
old-location: wsw\wsgetreaderposition.htm
tech.root: wsw
ms.assetid: 91e543f3-7325-4a90-9b99-c98918478853
ms.date: 12/05/2018
ms.keywords: WsGetReaderPosition, WsGetReaderPosition function [Web Services for Windows], webservices/WsGetReaderPosition, wsw.wsgetreaderposition
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
 - WsGetReaderPosition
 - webservices/WsGetReaderPosition
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
 - WsGetReaderPosition
---

# WsGetReaderPosition function


## -description

Returns the current position of the reader.  This can only be used on a reader 
        that is set to an XmlBuffer.

## -parameters

### -param reader [in]

The reader for which the current position will be obtained.

### -param nodePosition [out]

The current position of the reader.

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
</table>

## -remarks

See <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node_position">WS_XML_NODE_POSITION</a> for more information on using positions.