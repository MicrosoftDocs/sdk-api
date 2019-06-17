---
UID: NN:vidcap.IKsTopologyInfo
title: IKsTopologyInfo (vidcap.h)
author: windows-sdk-content
description: The IKsTopologyInfo interface enumerates the nodes in a stream class driver. The KsProxy filter exposes this interface. Applications can use this interface to examine the internal topology of a kernel-mode filter.
old-location: dshow\ikstopologyinfo.htm
tech.root: DirectShow
ms.assetid: 641a10fe-8e8c-4225-b05e-b09dfb5f2fee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKsTopologyInfo, IKsTopologyInfo interface [DirectShow], IKsTopologyInfo interface [DirectShow],described, IKsTopologyInfoInterface, dshow.ikstopologyinfo, vidcap/IKsTopologyInfo
ms.topic: interface
f1_keywords: ["vidcap/IKsTopologyInfo"]
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IKsTopologyInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IKsTopologyInfo interface


## -description



The <code>IKsTopologyInfo</code> interface enumerates the nodes in a stream class driver. The KsProxy filter exposes this interface. Applications can use this interface to examine the internal topology of a kernel-mode filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKsTopologyInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKsTopologyInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IKsTopologyInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-createnodeinstance">CreateNodeInstance</a>
</td>
<td align="left" width="63%">
Creates a COM object that represents a node in the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_category">get_Category</a>
</td>
<td align="left" width="63%">
Returns one of the filter categories for this stream class driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo">get_ConnectionInfo</a>
</td>
<td align="left" width="63%">
Returns information about one node connection in the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_nodename">get_NodeName</a>
</td>
<td align="left" width="63%">
Returns the name of the node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_nodetype">get_NodeType</a>
</td>
<td align="left" width="63%">
Returns the node type for a given node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_numcategories">get_NumCategories</a>
</td>
<td align="left" width="63%">
Returns the number of categories for this filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_numconnections">get_NumConnections</a>
</td>
<td align="left" width="63%">
Returns the number of node connections within the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_numnodes">get_NumNodes</a>
</td>
<td align="left" width="63%">
Returns the number of nodes in the filter.

</td>
</tr>
</table> 


## -remarks



In the Windows Driver Model, a kernel-streaming (KS) filter contains one or more <i>nodes</i>. Each node encapsulates a processing task that is applied to the stream. Nodes have inputs and outputs, which connect either to other nodes in the filter, or else to the filter's pins. In this way, the nodes resemble a miniature "filter graph" inside the filter, which may contain several possible data paths. Applications can use the <code>IKsTopologyInfo</code> interface to get information about the nodes and the node connections.

<img alt="KsFilter nodes" border="0" src="./images/ksproxynodes.png"/>

Some devices also support the <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-iselector">ISelector</a> interface for selecting input nodes. For example, if a video capture device has a camera and a tape transport, these could be represented as two nodes (see the previous diagram).

Include Vidcap.h from the Windows SDK or from the DirectX 9.0 SDK Update (Summer 2004) or later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/working-with-usb-dv-video-devices">Working with USB DV Video Devices</a>
 

 

