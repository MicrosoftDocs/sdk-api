---
UID: NF:webservices.WsGetReaderNode
title: WsGetReaderNode function
author: windows-sdk-content
description: The function returns the XML node at the current position of the XML reader.
old-location: wsw\wsgetreadernode.htm
old-project: wsw
ms.assetid: c8e5b5ea-f7b7-41ad-9669-7c88ec4ad28c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WsGetReaderNode, WsGetReaderNode function [Web Services for Windows], webservices/WsGetReaderNode, wsw.wsgetreadernode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetReaderNode
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsGetReaderNode function


## -description


The function returns the XML <a href="https://msdn.microsoft.com/98c40d57-ee71-40f8-9416-5b29adc30489">node</a> at the current position of the XML <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">reader</a>.
      


## -parameters




### -param xmlReader [in]

A pointer to the reader for which the current node will be obtained.  This must be valid WS_XML_READER object.


### -param node

A reference to a <a href="https://msdn.microsoft.com/98c40d57-ee71-40f8-9416-5b29adc30489">WS_XML_NODE</a> structure where the current node is returned.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.


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



The <a href="https://msdn.microsoft.com/eddef5db-432d-4615-9f0f-a712dffe42ab">nodeType</a> field of the node <a href="https://msdn.microsoft.com/98c40d57-ee71-40f8-9416-5b29adc30489">node</a> should be inspected
        to determine the kind of node returned.  The <b>node</b> may then be cast to the appropriate
        data structure to get the data.
      

<pre class="syntax" xml:space="preserve"><code>WS_XML_NODE* node;
if (SUCCEEDED(WsGetReaderNode(reader, &amp;node, error)))
{
    if (node-&gt;nodeType == WS_XML_NODE_TYPE_ELEMENT)
    {
        WS_XML_ELEMENT_NODE* elementNode = (WS_XML_ELEMENT_NODE*) node;
        // Refer to elementNode-&gt;localName, elementNode-&gt;ns
    }
}</code></pre>
The <a href="https://msdn.microsoft.com/eddef5db-432d-4615-9f0f-a712dffe42ab">nodeTypes</a> with extended structures include:
        <ul>
<li><b>WS_XML_NODE_TYPE_ELEMENT</b> =&gt; <a href="https://msdn.microsoft.com/32157ddf-ace2-49dc-85d7-b04e25e85693">WS_XML_ELEMENT_NODE</a>
</li>
<li><b>WS_XML_NODE_TYPE_TEXT</b>    =&gt; <a href="https://msdn.microsoft.com/be009607-8d5c-4e9b-9b42-84d1fdaa594d">WS_XML_TEXT_NODE</a>
</li>
<li><b>WS_XML_NODE_TYPE_COMMENT</b> =&gt; <a href="https://msdn.microsoft.com/e1a0b493-4537-465b-93bb-64672bc5b3d9">WS_XML_COMMENT_NODE</a>
</li>
</ul>


The node returned should not be modified and is only valid until the reader advances.
      For the attributes in a <a href="https://msdn.microsoft.com/32157ddf-ace2-49dc-85d7-b04e25e85693">WS_XML_ELEMENT_NODE</a> callers should not expect the
        attributes to appear in any particular order.
      



