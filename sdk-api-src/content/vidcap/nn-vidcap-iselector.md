---
UID: NN:vidcap.ISelector
title: ISelector
author: windows-sdk-content
description: The ISelector interface is used to select source nodes in a stream class driver.
old-location: dshow\iselector.htm
tech.root: DirectShow
ms.assetid: bd6e028c-ed6d-4dad-a276-c59ba9d88e87
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISelector, ISelector interface [DirectShow], ISelector interface [DirectShow],described, ISelectorInterface, dshow.iselector, vidcap/ISelector
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ISelector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISelector interface


## -description



The <code>ISelector</code> interface is used to select source nodes in a stream class driver. Applications can use this interface to select which input is active on the device. For example, if a USB video capture device has a camera and a tape transport, these inputs could be represented as source nodes.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISelector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISelector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISelector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff04e32f-7902-417e-b0d4-125914928679">get_NumSources</a>
</td>
<td align="left" width="63%">
Returns the number of source nodes connected to the selector node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae2b0e1a-1527-4634-b2f9-47c9519b55a6">get_SourceNodeId</a>
</td>
<td align="left" width="63%">
Returns the index of the active source node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cf6a406-eeb8-45ba-9c4c-0fdc6d6a30cf">put_SourceNodeId</a>
</td>
<td align="left" width="63%">
Activates a source node.

</td>
</tr>
</table> 


## -remarks



A kernel-streaming (KS) filter contains one or more <i>nodes</i>. Each node encapsulates a processing task that is applied to the stream. In the following diagram, nodes 1 and 2 are <i>source</i> nodes and node 3 is a <i>selector</i> node.

<img alt="KsProxy nodes" border="0" src="./images/ksproxynodes.png"/>

The source nodes represent input streams—for example, a camera or a tape transport. The selector node controls which stream is sent to the filter's output pin. To switch between inputs, an application would do the following:

<ol>
<li>Use the <a href="https://msdn.microsoft.com/641a10fe-8e8c-4225-b05e-b09dfb5f2fee">IKsTopologyInfo</a> interface to enumerate the nodes and discover the node types, identifiers, and names.</li>
<li>Call <a href="https://msdn.microsoft.com/f2c7ea1d-abd6-4179-b5b7-d89837ceecd7">IKsTopologyInfo::CreateNodeInstance</a> to create the selector node, passing in the node identifier and the interface identifier IID_ISelector. The method returns an <code>ISelector</code> interface pointer.</li>
<li>Use the <code>ISelector</code> interface to select the source node.</li>
</ol>
The <code>ISelector</code> interface is available if the selector node supports the PROPSETID_VIDCAP_SELECTOR property set. For more information, see the Windows DDK documentation.



