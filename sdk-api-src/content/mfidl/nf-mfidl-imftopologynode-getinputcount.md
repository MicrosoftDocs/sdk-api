---
UID: NF:mfidl.IMFTopologyNode.GetInputCount
title: IMFTopologyNode::GetInputCount (mfidl.h)
description: Retrieves the number of input streams that currently exist on this node.
helpviewer_keywords: ["84c079da-5de6-4c33-b0c7-5ffd017d5513","GetInputCount","GetInputCount method [Media Foundation]","GetInputCount method [Media Foundation]","IMFTopologyNode interface","IMFTopologyNode interface [Media Foundation]","GetInputCount method","IMFTopologyNode.GetInputCount","IMFTopologyNode::GetInputCount","mf.imftopologynode_getinputcount","mfidl/IMFTopologyNode::GetInputCount"]
old-location: mf\imftopologynode_getinputcount.htm
tech.root: mf
ms.assetid: 84c079da-5de6-4c33-b0c7-5ffd017d5513
ms.date: 12/05/2018
ms.keywords: 84c079da-5de6-4c33-b0c7-5ffd017d5513, GetInputCount, GetInputCount method [Media Foundation], GetInputCount method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetInputCount method, IMFTopologyNode.GetInputCount, IMFTopologyNode::GetInputCount, mf.imftopologynode_getinputcount, mfidl/IMFTopologyNode::GetInputCount
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
 - IMFTopologyNode::GetInputCount
 - mfidl/IMFTopologyNode::GetInputCount
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
 - IMFTopologyNode.GetInputCount
---

# IMFTopologyNode::GetInputCount


## -description

Retrieves the number of input streams that currently exist on this node.

## -parameters

### -param pcInputs [out]

Receives the number of input streams.

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

The input streams may or may not be connected to output streams on other nodes. To get the node that is connected to a specified input stream, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput">IMFTopologyNode::GetInput</a>.

The <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput">IMFTopologyNode::ConnectOutput</a> and <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setinputpreftype">IMFTopologyNode::SetInputPrefType</a> methods add new input streams as needed.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>