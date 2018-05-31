---
UID: NN:strmif.IDvdGraphBuilder
title: IDvdGraphBuilder
author: windows-sdk-content
description: The IDvdGraphBuilder interface builds a filter graph for DVD-Video playback.
old-location: dshow\idvdgraphbuilder.htm
old-project: DirectShow
ms.assetid: 2179e54a-c6e2-4837-9f89-be210bde9180
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IDvdGraphBuilder, IDvdGraphBuilder interface [DirectShow], IDvdGraphBuilder interface [DirectShow],described, IDvdGraphBuilderInterface, dshow.idvdgraphbuilder, strmif/IDvdGraphBuilder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdGraphBuilder
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdGraphBuilder interface


## -description



The <code>IDvdGraphBuilder</code> interface builds a filter graph for DVD-Video playback. The <a href="https://msdn.microsoft.com/c74cf1d8-2560-4302-ba68-8a1693f7ca6f">DVD Graph Builder</a> object implements this interface.

The <a href="https://msdn.microsoft.com/731d2f4b-2a54-451a-8d98-b5fdf47c1dc8">RenderDvdVideoVolume</a> method builds a DVD playback graph from the available software and hardware on the system. For information on how to build the DVD filter graph and obtain the pointers to all the necessary interfaces, see <a href="https://msdn.microsoft.com/1d2f8284-2deb-4207-b067-24a54d6b286c">Building the DVD Filter Graph</a>.

<div class="alert"><b>Note</b>  
           A DVD filter graph requires either a hardware or software MPEG-2 decoder.</div>
<div> </div>
Generally, you should not add, remove, connect, disconnect, or access individual filters in the graph created by <b>RenderDvdVideoVolume</b>, because doing so might confuse the cleanup code. The purpose of the <b>DvdGraphBuilder</b> object is to simplify the development of DVD-Video applications. If you need a specific type of graph for a particular solution, you should manually create the entire filter graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdGraphBuilder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvdGraphBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvdGraphBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e16cb767-87a9-49f6-a3a7-88166f2abe73">GetDvdInterface</a>
</td>
<td align="left" width="63%">
Retrieves interfaces from the DVD-Video playback graph to make DVD-Video playback development easier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f12140b-d10d-47d9-8bac-33fab084bff4">GetFiltergraph</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface for the filter graph used by the DVD-Video graph builder object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/731d2f4b-2a54-451a-8d98-b5fdf47c1dc8">RenderDvdVideoVolume</a>
</td>
<td align="left" width="63%">
Completes building a filter graph according to user specifications for playing a DVD-Video volume.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>
 

 

