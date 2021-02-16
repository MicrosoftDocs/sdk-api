---
UID: NF:mfidl.IMFTopologyNode.GetInput
title: IMFTopologyNode::GetInput (mfidl.h)
description: Retrieves the node that is connected to a specified input stream on this node.
helpviewer_keywords: ["49969e6d-c893-4f6f-8c1d-87d32405a65d","GetInput","GetInput method [Media Foundation]","GetInput method [Media Foundation]","IMFTopologyNode interface","IMFTopologyNode interface [Media Foundation]","GetInput method","IMFTopologyNode.GetInput","IMFTopologyNode::GetInput","mf.imftopologynode_getinput","mfidl/IMFTopologyNode::GetInput"]
old-location: mf\imftopologynode_getinput.htm
tech.root: mf
ms.assetid: 49969e6d-c893-4f6f-8c1d-87d32405a65d
ms.date: 12/05/2018
ms.keywords: 49969e6d-c893-4f6f-8c1d-87d32405a65d, GetInput, GetInput method [Media Foundation], GetInput method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetInput method, IMFTopologyNode.GetInput, IMFTopologyNode::GetInput, mf.imftopologynode_getinput, mfidl/IMFTopologyNode::GetInput
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
 - IMFTopologyNode::GetInput
 - mfidl/IMFTopologyNode::GetInput
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
 - IMFTopologyNode.GetInput
---

# IMFTopologyNode::GetInput


## -description

Retrieves the node that is connected to a specified input stream on this node.

## -parameters

### -param dwInputIndex [in]

Zero-based index of an input stream on this node.

### -param ppUpstreamNode [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface of the node that is connected to the specified input stream. The caller must release the interface.

### -param pdwOutputIndexOnUpstreamNode [out]

Receives the index of the output stream that is connected to this node's input stream.

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
The index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified input stream is not connected to another node.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>