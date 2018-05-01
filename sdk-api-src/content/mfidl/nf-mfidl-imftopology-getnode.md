---
UID: NF:mfidl.IMFTopology.GetNode
title: IMFTopology::GetNode method
author: windows-driver-content
description: Gets a node in the topology, specified by index.
old-location: mf\imftopology_getnode.htm
old-project: medfound
ms.assetid: 97053d10-5ac7-40c0-b46b-77d401284d58
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 97053d10-5ac7-40c0-b46b-77d401284d58, GetNode method [Media Foundation], GetNode method [Media Foundation], IMFTopology interface, GetNode,IMFTopology.GetNode, IMFTopology, IMFTopology interface [Media Foundation], GetNode method, IMFTopology::GetNode, mf.imftopology_getnode, mfidl/IMFTopology::GetNode
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
-	IMFTopology.GetNode
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopology::GetNode method


## -description



          Gets a node in the topology, specified by index.
        


## -parameters




### -param wIndex [in]


            The zero-based index of the node. To get the number of nodes in the topology, call <a href="https://msdn.microsoft.com/87378088-1d7a-4ad7-942f-69b6cfc4e573">IMFTopology::GetNodeCount</a>.
          


### -param ppNode [out]


            Receives a pointer to the node's <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface. The caller must release the pointer.
          


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

                The index is less than zero.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">

                No node can be found at the index <i>wIndex</i>.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

