---
UID: NF:webservices.WsCopyNode
title: WsCopyNode function (webservices.h)
description: Copies the current node from the specified XML reader to the specified XML writer.
helpviewer_keywords: ["WsCopyNode","WsCopyNode function [Web Services for Windows]","webservices/WsCopyNode","wsw.wscopynode"]
old-location: wsw\wscopynode.htm
tech.root: wsw
ms.assetid: 36078f7d-4c1f-4b8a-9f44-cd4949b7de04
ms.date: 12/05/2018
ms.keywords: WsCopyNode, WsCopyNode function [Web Services for Windows], webservices/WsCopyNode, wsw.wscopynode
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
 - WsCopyNode
 - webservices/WsCopyNode
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
 - WsCopyNode
---

# WsCopyNode function


## -description

Copies the current node from the specified <a href="/windows/desktop/wsw/xml-reader">XML reader</a> to the specified <a href="/windows/desktop/wsw/xml-writer">XML writer</a>.

## -parameters

### -param writer [in]

Pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> to which to copy the XML node.

### -param reader [in]

Pointer to the <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a>   from which to copy the XML node.

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
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

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

If the current node type is WS_XML_NODE_TYPE_ELEMENT,the current node,
        all its children, and the corresponding end element, are copied to the XML writer.
      

If the current node type is WS_XML_NODE_TYPE_BOF, nodes are copied
        until a node of type WS_XML_NODE_TYPE_EOF is reached.
      For information on node types, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_node_type">WS_XML_NODE_TYPE</a> enumeration.

The reader will be positioned on the node following the node copied.