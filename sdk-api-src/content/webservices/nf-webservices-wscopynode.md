---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WsCopyNode function


## -description



Copies the current node from the specified <a href="https://msdn.microsoft.com/1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2">XML reader</a> to the specified <a href="https://msdn.microsoft.com/69d50793-1d5b-4fc7-bf69-128f8e23a98d">XML writer</a>. 
      




## -parameters




### -param writer [in]

Pointer to the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> to which to copy the XML node.
        


### -param reader [in]

Pointer to the <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a>   from which to copy the XML node.
        


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                


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
      For information on node types, see the <a href="https://msdn.microsoft.com/eddef5db-432d-4615-9f0f-a712dffe42ab">WS_XML_NODE_TYPE</a> enumeration.


        The reader will be positioned on the node following the node copied.
      



