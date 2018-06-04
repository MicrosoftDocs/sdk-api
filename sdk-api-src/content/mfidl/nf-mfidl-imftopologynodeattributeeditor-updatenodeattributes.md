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

# IMFTopologyNodeAttributeEditor::UpdateNodeAttributes


## -description



Updates the attributes of one or more nodes in the current topology.




## -parameters




### -param TopoId [in]

Reserved.


### -param cUpdates [in]

The number of elements in the <i>pUpdates</i> array.


### -param pUpdates [in]

Pointer to an array of <a href="https://msdn.microsoft.com/94c89067-9b3e-4d24-9192-a68e284c5d99">MFTOPONODE_ATTRIBUTE_UPDATE</a> structures. Each element of the array updates one attribute on a node.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Currently the only attribute that can be updated is the <a href="https://msdn.microsoft.com/c1022538-ea9f-41e9-9075-c106e8b16b7b">MF_TOPONODE_MEDIASTOP</a> attribute. The method ignores any other attributes.




## -see-also




<a href="https://msdn.microsoft.com/9ab384b9-0ce9-428c-a683-b09dbd4e07d9">IMFTopologyNodeAttributeEditor</a>
 

 

