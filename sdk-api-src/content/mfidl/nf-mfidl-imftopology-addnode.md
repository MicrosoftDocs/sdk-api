---
UID: NF:mfidl.IMFTopology.AddNode
title: IMFTopology::AddNode
author: windows-sdk-content
description: Adds a node to the topology.
old-location: mf\imftopology_addnode.htm
old-project: medfound
ms.assetid: 5e519524-f5c5-4d4d-922f-166f9e616631
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 5e519524-f5c5-4d4d-922f-166f9e616631, AddNode, AddNode method [Media Foundation], AddNode method [Media Foundation],IMFTopology interface, IMFTopology interface [Media Foundation],AddNode method, IMFTopology.AddNode, IMFTopology::AddNode, mf.imftopology_addnode, mfidl/IMFTopology::AddNode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTopology.AddNode
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopology::AddNode


## -description



Adds a node to the topology.




## -parameters




### -param pNode [in]

Pointer to the node's <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pNode</i> is invalid, possibly because the node already exists in the topology.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

