---
UID: NN:strmif.ICaptureGraphBuilder2
title: ICaptureGraphBuilder2
author: windows-driver-content
description: The ICaptureGraphBuilder2 interface builds capture graphs and other custom filter graphs.
old-location: dshow\icapturegraphbuilder2.htm
old-project: DirectShow
ms.assetid: abdf6fb2-e98f-4df8-98ec-06d33798abb5
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ICaptureGraphBuilder2, ICaptureGraphBuilder2 interface [DirectShow], ICaptureGraphBuilder2 interface [DirectShow], described, ICaptureGraphBuilder2Interface, dshow.icapturegraphbuilder2, strmif/ICaptureGraphBuilder2
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ICaptureGraphBuilder2
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICaptureGraphBuilder2 interface


## -description



The <code>ICaptureGraphBuilder2</code> interface builds capture graphs and other custom filter graphs. The <a href="https://msdn.microsoft.com/df59afcf-6e11-463f-80ac-8b1fcc496d5b">Capture Graph Builder</a> object implements this interface.

<div class="alert"><b>Note</b>  By default, the <code>ICaptureGraphBuilder2</code> interface does not use the Video Mixing Renderer (VMR), Enhanced Video Renderer (EVR) or <a href="https://msdn.microsoft.com/d70558a5-9820-432a-b4f3-ccf7bb2a34d5">Video Port Manager</a> filters.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICaptureGraphBuilder2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICaptureGraphBuilder2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICaptureGraphBuilder2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e61459bd-cccb-4857-b336-82d23135fa16">AllocCapFile</a>
</td>
<td align="left" width="63%">
Preallocates a capture file to a specified size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5c91444-6ddb-403c-bff5-33d9ce91fae3">ControlStream</a>
</td>
<td align="left" width="63%">
Sets the start and stop times for one or more streams of captured data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4084b12-b082-45c2-9f07-625b980c7e4c">CopyCaptureFile</a>
</td>
<td align="left" width="63%">
Copies the valid media data from a capture file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/931b42bf-25d6-4f0a-8c45-baf8ed65e302">FindInterface</a>
</td>
<td align="left" width="63%">
Searches the graph for a specified interface, starting from a specified filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f74e55d4-2d51-47a9-aca8-dd4e616a6253">FindPin</a>
</td>
<td align="left" width="63%">
Retrieves a particular pin on a filter, or determines whether a given pin matches the specified criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91136a71-cfda-4aa5-ba6c-d1ce6cbef3c1">GetFiltergraph</a>
</td>
<td align="left" width="63%">
Retrieves the filter graph that the builder is using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fb5f13c-2bf5-463b-a209-77129a159bd6">RenderStream</a>
</td>
<td align="left" width="63%">
Connects an output pin on a source filter to a rendering filter, optionally through a compression filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6193ece8-cdf1-44f5-9619-16380352193f">SetFiltergraph</a>
</td>
<td align="left" width="63%">
Specifies a filter graph for the capture graph builder to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b81a79c1-a6f2-4c80-ae86-095fb9f78673">SetOutputFileName</a>
</td>
<td align="left" width="63%">
Creates the file writing section of the filter graph.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0329c4f0-ee6f-423e-b38b-169204e3a31c">Building Graphs with the Capture Graph Builder</a>



<a href="https://msdn.microsoft.com/7c91e560-ac69-47e1-a921-c312b77ecadc">Recompressing an AVI File</a>



<a href="https://msdn.microsoft.com/92051a84-5011-42ed-be68-e8841552ca1b">Video Capture</a>
 

 

