---
UID: NN:strmif.ICaptureGraphBuilder
title: ICaptureGraphBuilder
author: windows-sdk-content
description: Note  This interface has been deprecated.
old-location: dshow\icapturegraphbuilder.htm
tech.root: DirectShow
ms.assetid: 64ee80cd-9f63-4f38-853a-1ecfc03e6076
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICaptureGraphBuilder, ICaptureGraphBuilder interface [DirectShow], ICaptureGraphBuilder interface [DirectShow],described, ICaptureGraphBuilderInterface, dshow.icapturegraphbuilder, strmif/ICaptureGraphBuilder
ms.topic: interface
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - strmif.h
api_name:
 - ICaptureGraphBuilder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICaptureGraphBuilder interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use the <a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2</a> interface.</div>
<div> </div>
The <code>ICaptureGraphBuilder</code> interface enables you to build capture graphs, preview graphs, file recompression graphs, or other custom graphs.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICaptureGraphBuilder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICaptureGraphBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICaptureGraphBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/116ee108-ae03-4761-84db-9391ebddaae2">AllocCapFile</a>
</td>
<td align="left" width="63%">
Preallocates a capture file to a specified size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d7d3a4d-3071-4829-99df-f0bcc9197b38">ControlStream</a>
</td>
<td align="left" width="63%">
Sends stream control messages to the pin of the specified category on one or more capture filters in a graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6eb4a3ed-6914-4839-ab1f-18510483ab49">CopyCaptureFile</a>
</td>
<td align="left" width="63%">
Copies the valid media data from the preallocated capture file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23fe9a5a-0f3b-44b3-9d37-6889214657bf">FindInterface</a>
</td>
<td align="left" width="63%">
Looks for the specified interface on the filter, upstream and downstream from the filter, and, optionally, only on the output pin of the given category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cb43dca-79f1-4467-8e17-6f2a0b4db785">GetFiltergraph</a>
</td>
<td align="left" width="63%">
Retrieves the filter graph that the builder is using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b174f31-d7bb-4934-9d5b-2e4fd6ae8bf5">RenderStream</a>
</td>
<td align="left" width="63%">
Connects a source filter's pin, of an optionally specified category, to the rendering filter, and optionally through another filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01cb7f09-6ff2-46c1-b6f2-76583785b242">SetFiltergraph</a>
</td>
<td align="left" width="63%">
Tells the graph builder object which filter graph to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f410465f-c560-49ab-9194-66d708274f77">SetOutputFileName</a>
</td>
<td align="left" width="63%">
Creates the rendering section of the filter graph, which will save bits to disk with the specified file name.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>
 

 

