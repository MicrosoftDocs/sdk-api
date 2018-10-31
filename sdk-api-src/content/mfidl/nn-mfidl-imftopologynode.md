---
UID: NN:mfidl.IMFTopologyNode
title: IMFTopologyNode
author: windows-sdk-content
description: Represents a node in a topology.
old-location: mf\imftopologynode.htm
tech.root: medfound
ms.assetid: 01d7eb7c-a3d3-4924-a8ec-a67e9dc17424
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 01d7eb7c-a3d3-4924-a8ec-a67e9dc17424, IMFTopologyNode, IMFTopologyNode interface [Media Foundation], IMFTopologyNode interface [Media Foundation],described, mf.imftopologynode, mfidl/IMFTopologyNode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
</ul>To create a new node, call the <a href="https://msdn.microsoft.com/67c32232-09cb-4098-b80b-4b93ee121190">MFCreateTopologyNode</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTopologyNode</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFTopologyNode</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/90322fbc-e3de-4801-b10b-63ce538fc83f">CloneFrom</a>
</td>
<td align="left" width="63%">
Copies the data from another topology node into this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2340fd87-27ea-4f98-97e3-48b9506251a9">ConnectOutput</a>
</td>
<td align="left" width="63%">
Connects an output stream from this node to the input stream of another node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77b91797-d9a7-40da-827d-6e2a347112dc">DisconnectOutput</a>
</td>
<td align="left" width="63%">
Disconnects an output stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49969e6d-c893-4f6f-8c1d-87d32405a65d">GetInput</a>
</td>
<td align="left" width="63%">
Retrieves the node that is connected to a specified input stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84c079da-5de6-4c33-b0c7-5ffd017d5513">GetInputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of input streams that currently exist on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34849803-2b56-457a-920b-b5f2e208ce2e">GetInputPrefType</a>
</td>
<td align="left" width="63%">
Retrieves the preferred media type for an input stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64b2d2b4-1f00-412d-8188-fa361dc317a1">GetNodeType</a>
</td>
<td align="left" width="63%">
Returns the node type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/039d8009-5e5a-4503-9908-7317bc2bf412">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves the object associated with this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d947d92-4669-4857-bd61-10fa8ebd2598">GetOutput</a>
</td>
<td align="left" width="63%">
Retrieves the node that is connected to a specified output stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc964c38-9dac-491f-9d70-b1ba7b7001ad">GetOutputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of output streams that currently exist on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/972052ca-1d87-4fa4-abeb-6e74ba6c9368">GetOutputPrefType</a>
</td>
<td align="left" width="63%">
Retrieves the preferred media type for an output stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c0e5be9-6481-4132-ad5b-9db13fb07391">GetTopoNodeID</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b02cf739-97a9-4bb0-abb1-0da491857c50">RemoteGetInputPrefType</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/34849803-2b56-457a-920b-b5f2e208ce2e">GetInputPrefType</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56fbbf14-0c55-4f98-bcda-7f434cff803c">RemoteGetOutputPrefType</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/972052ca-1d87-4fa4-abeb-6e74ba6c9368">GetOutputPrefType</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/348b3cba-8c8c-4df9-8cb9-b69cd140cffb">SetInputPrefType</a>
</td>
<td align="left" width="63%">
Sets the preferred media type for an input stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbef706d-a4a0-4ff3-bfdb-8ba39d70617c">SetObject</a>
</td>
<td align="left" width="63%">
Sets the object associated with this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/948fd64d-e3d8-45de-aaab-b052d9f0b9d8">SetOutputPrefType</a>
</td>
<td align="left" width="63%">
Sets the preferred media type for an output stream on this node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80efa004-d739-4f9a-9ea3-8bf7d97f0a7d">SetTopoNodeID</a>
</td>
<td align="left" width="63%">
Sets the identifier for the node.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>



<a href="https://msdn.microsoft.com/584c0670-9051-4d03-9635-c8fadc8798c3">Topology Node Attributes</a>
 

 

