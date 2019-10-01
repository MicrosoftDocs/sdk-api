---
UID: NN:mfidl.IMFTopologyNode
title: IMFTopologyNode (mfidl.h)
author: windows-sdk-content
description: Represents a node in a topology.
old-location: mf\imftopologynode.htm
tech.root: medfound
ms.assetid: 01d7eb7c-a3d3-4924-a8ec-a67e9dc17424
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 01d7eb7c-a3d3-4924-a8ec-a67e9dc17424, IMFTopologyNode, IMFTopologyNode interface [Media Foundation], IMFTopologyNode interface [Media Foundation],described, mf.imftopologynode, mfidl/IMFTopologyNode
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFTopologyNode"
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
 - IMFTopologyNode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTopologyNode interface


## -description


Represents a node in a topology. The following node types are supported:
<ul>
<li>Output node. Represents a media sink.
            </li>
<li>Source node. Represents a media stream.
            </li>
<li>Transform node. Represents a Media Foundation Transform (MFT).
            </li>
<li>Tee node. Delivers a media stream to two or more nodes.
            </li>
</ul>To create a new node, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode">MFCreateTopologyNode</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTopologyNode</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFTopologyNode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTopologyNode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-clonefrom">CloneFrom</a>
</td>
<td align="left" width="63%">
Copies the data from another topology node into this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput">ConnectOutput</a>
</td>
<td align="left" width="63%">
Connects an output stream from this node to the input stream of another node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-disconnectoutput">DisconnectOutput</a>
</td>
<td align="left" width="63%">
Disconnects an output stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput">GetInput</a>
</td>
<td align="left" width="63%">
Retrieves the node that is connected to a specified input stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputcount">GetInputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of input streams that currently exist on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype">GetInputPrefType</a>
</td>
<td align="left" width="63%">
Retrieves the preferred media type for an input stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getnodetype">GetNodeType</a>
</td>
<td align="left" width="63%">
Returns the node type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves the object associated with this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutput">GetOutput</a>
</td>
<td align="left" width="63%">
Retrieves the node that is connected to a specified output stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputcount">GetOutputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of output streams that currently exist on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype">GetOutputPrefType</a>
</td>
<td align="left" width="63%">
Retrieves the preferred media type for an output stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid">GetTopoNodeID</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imftopologynode-remotegetinputpreftype">RemoteGetInputPrefType</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype">GetInputPrefType</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imftopologynode-remotegetoutputpreftype">RemoteGetOutputPrefType</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype">GetOutputPrefType</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setinputpreftype">SetInputPrefType</a>
</td>
<td align="left" width="63%">
Sets the preferred media type for an input stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject">SetObject</a>
</td>
<td align="left" width="63%">
Sets the object associated with this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setoutputpreftype">SetOutputPrefType</a>
</td>
<td align="left" width="63%">
Sets the preferred media type for an output stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-settoponodeid">SetTopoNodeID</a>
</td>
<td align="left" width="63%">
Sets the identifier for the node.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topologies">Topologies</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topology-node-attributes">Topology Node Attributes</a>
 

 

