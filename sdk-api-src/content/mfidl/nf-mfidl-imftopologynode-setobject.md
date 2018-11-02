---
UID: NF:mfidl.IMFTopologyNode.SetObject
title: IMFTopologyNode::SetObject
author: windows-sdk-content
description: Sets the object associated with this node.
old-location: mf\imftopologynode_setobject.htm
tech.root: medfound
ms.assetid: bbef706d-a4a0-4ff3-bfdb-8ba39d70617c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMFTopologyNode interface [Media Foundation],SetObject method, IMFTopologyNode.SetObject, IMFTopologyNode::SetObject, SetObject, SetObject method [Media Foundation], SetObject method [Media Foundation],IMFTopologyNode interface, bbef706d-a4a0-4ff3-bfdb-8ba39d70617c, mf.imftopologynode_setobject, mfidl/IMFTopologyNode::SetObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTopologyNode.SetObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

