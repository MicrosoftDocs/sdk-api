---
UID: NF:mfidl.IMFTopologyNode.ConnectOutput
title: IMFTopologyNode::ConnectOutput (mfidl.h)
description: Connects an output stream from this node to the input stream of another node.
helpviewer_keywords: ["2340fd87-27ea-4f98-97e3-48b9506251a9","ConnectOutput","ConnectOutput method [Media Foundation]","ConnectOutput method [Media Foundation]","IMFTopologyNode interface","IMFTopologyNode interface [Media Foundation]","ConnectOutput method","IMFTopologyNode.ConnectOutput","IMFTopologyNode::ConnectOutput","mf.imftopologynode_connectoutput","mfidl/IMFTopologyNode::ConnectOutput"]
old-location: mf\imftopologynode_connectoutput.htm
tech.root: mf
ms.assetid: 2340fd87-27ea-4f98-97e3-48b9506251a9
ms.date: 12/05/2018
ms.keywords: 2340fd87-27ea-4f98-97e3-48b9506251a9, ConnectOutput, ConnectOutput method [Media Foundation], ConnectOutput method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],ConnectOutput method, IMFTopologyNode.ConnectOutput, IMFTopologyNode::ConnectOutput, mf.imftopologynode_connectoutput, mfidl/IMFTopologyNode::ConnectOutput
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
 - IMFTopologyNode::ConnectOutput
 - mfidl/IMFTopologyNode::ConnectOutput
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
 - IMFTopologyNode.ConnectOutput
---

# IMFTopologyNode::ConnectOutput


## -description

Connects an output stream from this node to the input stream of another node.

## -parameters

### -param dwOutputIndex [in]

Zero-based index of the output stream on this node.

### -param pDownstreamNode [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface of the node to connect to.

### -param dwInputIndexOnDownstreamNode [in]

Zero-based index of the input stream on the other node.

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
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter.

</td>
</tr>
</table>

## -remarks

Node connections represent data flow from one node to the next. The streams are logical, and are specified by index.

If the node is already connected at the specified output, the method breaks the existing connection. If <i>dwOutputIndex</i> or <i>dwInputIndexOnDownstreamNode</i> specify streams that do not exist yet, the method adds as many streams as needed.

This method checks for certain invalid conditions:

<ul>
<li>
An output node cannot have any output connections. If you call this method on an output node, the method returns E_FAIL.

</li>
<li>
A node cannot be connected to itself. If <i>pDownstreamNode</i> specifies the same node as the method call, the method returns E_INVALIDARG.

</li>
</ul>
However, if the method succeeds, it does not guarantee that the node connection is valid. It is possible to create a partial topology that the topology loader cannot resolve. If so, the <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load">IMFTopoLoader::Load</a> method will fail.

To break an existing node connection, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-disconnectoutput">IMFTopologyNode::DisconnectOutput</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>