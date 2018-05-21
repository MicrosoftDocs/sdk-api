---
UID: NF:mfidl.IMFTopology.GetNodeByID
title: IMFTopology::GetNodeByID
author: windows-driver-content
description: Gets a node in the topology, specified by node identifier.
old-location: mf\imftopology_getnodebyid.htm
old-project: medfound
ms.assetid: 34c8326f-bd34-4bf6-9171-a1ed3191b85e
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 34c8326f-bd34-4bf6-9171-a1ed3191b85e, GetNodeByID, GetNodeByID method [Media Foundation], GetNodeByID method [Media Foundation],IMFTopology interface, IMFTopology interface [Media Foundation],GetNodeByID method, IMFTopology.GetNodeByID, IMFTopology::GetNodeByID, mf.imftopology_getnodebyid, mfidl/IMFTopology::GetNodeByID
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFTopology.GetNodeByID
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopology::GetNodeByID


## -description


Gets a node in the topology, specified by node identifier.


## -parameters




### -param qwTopoNodeID [in]


            The identifier of the node to retrieve. To get a node's identifier, call <a href="https://msdn.microsoft.com/9c0e5be9-6481-4132-ad5b-9db13fb07391">IMFTopologyNode::GetTopoNodeID</a>.
          


### -param ppNode [out]


            Receives a pointer to the node's <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface. The caller must release the interface.
          


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
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">

                The topology does not contain a node with this identifier.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a>



<a href="https://msdn.microsoft.com/a6d9246a-0cc6-4dbd-affa-e7d0bbddb008">TOPOID</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

