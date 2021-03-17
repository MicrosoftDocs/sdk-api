---
UID: NF:mfidl.IMFTopology.GetNode
title: IMFTopology::GetNode (mfidl.h)
description: Gets a node in the topology, specified by index.
helpviewer_keywords: ["97053d10-5ac7-40c0-b46b-77d401284d58","GetNode","GetNode method [Media Foundation]","GetNode method [Media Foundation]","IMFTopology interface","IMFTopology interface [Media Foundation]","GetNode method","IMFTopology.GetNode","IMFTopology::GetNode","mf.imftopology_getnode","mfidl/IMFTopology::GetNode"]
old-location: mf\imftopology_getnode.htm
tech.root: mf
ms.assetid: 97053d10-5ac7-40c0-b46b-77d401284d58
ms.date: 12/05/2018
ms.keywords: 97053d10-5ac7-40c0-b46b-77d401284d58, GetNode, GetNode method [Media Foundation], GetNode method [Media Foundation],IMFTopology interface, IMFTopology interface [Media Foundation],GetNode method, IMFTopology.GetNode, IMFTopology::GetNode, mf.imftopology_getnode, mfidl/IMFTopology::GetNode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTopology::GetNode
 - mfidl/IMFTopology::GetNode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTopology.GetNode
---

# IMFTopology::GetNode


## -description

Gets a node in the topology, specified by index.

## -parameters

### -param wIndex [in]

The zero-based index of the node. To get the number of nodes in the topology, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodecount">IMFTopology::GetNodeCount</a>.

### -param ppNode [out]

Receives a pointer to the node's <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface. The caller must release the pointer.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>