---
UID: NF:mfidl.IMFTopologyNode.GetOutputPrefType
title: IMFTopologyNode::GetOutputPrefType (mfidl.h)
description: Retrieves the preferred media type for an output stream on this node.
helpviewer_keywords: ["972052ca-1d87-4fa4-abeb-6e74ba6c9368","GetOutputPrefType","GetOutputPrefType method [Media Foundation]","GetOutputPrefType method [Media Foundation]","IMFTopologyNode interface","IMFTopologyNode interface [Media Foundation]","GetOutputPrefType method","IMFTopologyNode.GetOutputPrefType","IMFTopologyNode::GetOutputPrefType","mf.imftopologynode_getoutputpreftype","mfidl/IMFTopologyNode::GetOutputPrefType"]
old-location: mf\imftopologynode_getoutputpreftype.htm
tech.root: mf
ms.assetid: 972052ca-1d87-4fa4-abeb-6e74ba6c9368
ms.date: 12/05/2018
ms.keywords: 972052ca-1d87-4fa4-abeb-6e74ba6c9368, GetOutputPrefType, GetOutputPrefType method [Media Foundation], GetOutputPrefType method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetOutputPrefType method, IMFTopologyNode.GetOutputPrefType, IMFTopologyNode::GetOutputPrefType, mf.imftopologynode_getoutputpreftype, mfidl/IMFTopologyNode::GetOutputPrefType
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
 - IMFTopologyNode::GetOutputPrefType
 - mfidl/IMFTopologyNode::GetOutputPrefType
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
 - IMFTopologyNode.GetOutputPrefType
---

# IMFTopologyNode::GetOutputPrefType


## -description

Retrieves the preferred media type for an output stream on this node.

## -parameters

### -param dwOutputIndex [in]

Zero-based index of the output stream.

### -param ppType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type. The caller must release the interface.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
This node does not have a preferred output type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This node is an output node.

</td>
</tr>
</table>

## -remarks

Output nodes cannot have outputs. If this method is called on an output node, it returns E_NOTIMPL.

The preferred output type provides a hint to the topology loader. In a fully resolved topology, there is no guarantee that every topology node will have a preferred output type. To get the actual media type for a node, you must get a pointer to the node's underlying object. (For more information, see <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_topology_type">MF_TOPOLOGY_TYPE</a> enumeration.)

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>