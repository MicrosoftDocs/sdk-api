---
UID: NF:mfidl.IMFTopologyNode.DisconnectOutput
title: IMFTopologyNode::DisconnectOutput (mfidl.h)
description: Disconnects an output stream on this node.
helpviewer_keywords: ["77b91797-d9a7-40da-827d-6e2a347112dc","DisconnectOutput","DisconnectOutput method [Media Foundation]","DisconnectOutput method [Media Foundation]","IMFTopologyNode interface","IMFTopologyNode interface [Media Foundation]","DisconnectOutput method","IMFTopologyNode.DisconnectOutput","IMFTopologyNode::DisconnectOutput","mf.imftopologynode_disconnectoutput","mfidl/IMFTopologyNode::DisconnectOutput"]
old-location: mf\imftopologynode_disconnectoutput.htm
tech.root: mf
ms.assetid: 77b91797-d9a7-40da-827d-6e2a347112dc
ms.date: 12/05/2018
ms.keywords: 77b91797-d9a7-40da-827d-6e2a347112dc, DisconnectOutput, DisconnectOutput method [Media Foundation], DisconnectOutput method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],DisconnectOutput method, IMFTopologyNode.DisconnectOutput, IMFTopologyNode::DisconnectOutput, mf.imftopologynode_disconnectoutput, mfidl/IMFTopologyNode::DisconnectOutput
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
 - IMFTopologyNode::DisconnectOutput
 - mfidl/IMFTopologyNode::DisconnectOutput
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
 - IMFTopologyNode.DisconnectOutput
---

# IMFTopologyNode::DisconnectOutput


## -description

Disconnects an output stream on this node.

## -parameters

### -param dwOutputIndex [in]

Zero-based index of the output stream to disconnect.

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
The <i>dwOutputIndex</i> parameter is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified output stream is not connected to another node.

</td>
</tr>
</table>

## -remarks

If the specified output stream is connected to another node, this method breaks the connection.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>