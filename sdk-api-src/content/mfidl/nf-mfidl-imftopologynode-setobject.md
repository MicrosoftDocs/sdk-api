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

# IMFTopologyNode::SetObject


## -description



Sets the object associated with this node.




## -parameters




### -param pObject [in]

A pointer to the object's <b>IUnknown</b> interface. Use the value <b>NULL</b> to clear an object that was previous set.


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



All node types support this method, but the object pointer is not used by every node type.

<table>
<tr>
<th>Node type</th>
<th>Object pointer</th>
</tr>
<tr>
<td>Source node.</td>
<td>Not used.</td>
</tr>
<tr>
<td>Transform node.</td>
<td>
<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> or <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface.</td>
</tr>
<tr>
<td>Output node</td>
<td>
<a href="https://msdn.microsoft.com/fe403cab-b901-4c8e-a23c-788ee65c4689">IMFStreamSink</a> or <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface.</td>
</tr>
<tr>
<td>Tee node.</td>
<td>Not used.</td>
</tr>
</table>
 

If the object supports <b>IPersist</b>, <b>IPersistStorage</b>, or <b>IPersistPropertyBag</b>, the method gets the object's CLSID and sets the <a href="https://msdn.microsoft.com/6aa6e649-d23d-4d8d-be80-2b8814b07a57">MF_TOPONODE_TRANSFORM_OBJECTID</a> attribute on the node.




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

