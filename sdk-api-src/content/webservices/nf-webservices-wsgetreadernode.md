---
UID: NF:webservices.WsGetReaderNode
title: WsGetReaderNode function (webservices.h)
description: The function returns the XML node at the current position of the XML reader.
helpviewer_keywords: ["WsGetReaderNode","WsGetReaderNode function [Web Services for Windows]","webservices/WsGetReaderNode","wsw.wsgetreadernode"]
old-location: wsw\wsgetreadernode.htm
tech.root: wsw
ms.assetid: c8e5b5ea-f7b7-41ad-9669-7c88ec4ad28c
ms.date: 12/05/2018
ms.keywords: WsGetReaderNode, WsGetReaderNode function [Web Services for Windows], webservices/WsGetReaderNode, wsw.wsgetreadernode
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
 - WsGetReaderNode
 - webservices/WsGetReaderNode
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
 - WsGetReaderNode
---

# WsGetReaderNode function


## -description

The function returns the XML <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node">node</a> at the current position of the XML <a href="/windows/desktop/wsw/ws-xml-reader">reader</a>.

## -parameters

### -param xmlReader [in]

A pointer to the reader for which the current node will be obtained.  This must be valid WS_XML_READER object.

### -param node

A reference to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node">WS_XML_NODE</a> structure where the current node is returned.

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
</table>

## -remarks

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_node_type">nodeType</a> field of the node <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node">node</a> should be inspected
        to determine the kind of node returned.  The <b>node</b> may then be cast to the appropriate
        data structure to get the data.
      


``` syntax
WS_XML_NODE* node;
if (SUCCEEDED(WsGetReaderNode(reader, &node, error)))
{
    if (node->nodeType == WS_XML_NODE_TYPE_ELEMENT)
    {
        WS_XML_ELEMENT_NODE* elementNode = (WS_XML_ELEMENT_NODE*) node;
        // Refer to elementNode->localName, elementNode->ns
    }
}
```

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_node_type">nodeTypes</a> with extended structures include:
        <ul>
<li><b>WS_XML_NODE_TYPE_ELEMENT</b> =&gt; <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_element_node">WS_XML_ELEMENT_NODE</a>
</li>
<li><b>WS_XML_NODE_TYPE_TEXT</b>    =&gt; <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_text_node">WS_XML_TEXT_NODE</a>
</li>
<li><b>WS_XML_NODE_TYPE_COMMENT</b> =&gt; <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_comment_node">WS_XML_COMMENT_NODE</a>
</li>
</ul>


The node returned should not be modified and is only valid until the reader advances.
      For the attributes in a <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_element_node">WS_XML_ELEMENT_NODE</a> callers should not expect the
        attributes to appear in any particular order.
