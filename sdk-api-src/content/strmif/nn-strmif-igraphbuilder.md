---
UID: NN:strmif.IGraphBuilder
title: IGraphBuilder
author: windows-sdk-content
description: This interface provides methods that enable an application to build a filter graph.
old-location: dshow\igraphbuilder.htm
tech.root: DirectShow
ms.assetid: 54ed8ac8-4821-4c0c-9fb9-789c70dbca37
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IGraphBuilder, IGraphBuilder interface [DirectShow], IGraphBuilder interface [DirectShow],described, IGraphBuilderInterface, dshow.igraphbuilder, strmif/IGraphBuilder
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IGraphBuilder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGraphBuilder interface


## -description



This interface provides methods that enable an application to build a filter graph. The <a href="https://msdn.microsoft.com/b1a53193-27c6-4e86-a5b9-f3c1e4401690">Filter Graph Manager</a> implements this interface.

The <b>IGraphBuilder</b> interface inherits from the <a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph</a> interface. <b>IFilterGraph</b> provides basic operations, such as adding a filter to the graph or connecting two pins. <b>IGraphBuilder</b> adds further methods that construct graphs from partial information. For example, the <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a> method builds a graph for file playback, given the name of the file. The <a href="https://msdn.microsoft.com/de3adac7-ff99-4415-9afc-e25ad420df59">IGraphBuilder::Render</a> method renders data from an output pin by connecting new filters to the pin.

Using these methods, an application does not need to specify every filter and pin connection in the graph. Instead, the Filter Graph Manager selects filters that are registered on the user's system, adds them to the graph, and connects them. For more information, see <a href="https://msdn.microsoft.com/938ba1b0-822e-4871-8786-b7eeee243867">Intelligent Connect</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGraphBuilder</b> interface inherits from <a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph</a>. <b>IGraphBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGraphBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9a46959-afa0-4e12-80c3-c4b95feb96e5">Abort</a>
</td>
<td align="left" width="63%">
Requests that the graph builder return as soon as possible from its current task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed4d7fc6-558b-474f-ae8d-58aa8479b4d2">AddSourceFilter</a>
</td>
<td align="left" width="63%">
Adds a source filter to the filter graph for a specific file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ddcbb73-8220-4d70-9ab3-58d99fa8a958">Connect</a>
</td>
<td align="left" width="63%">
Connects two pins. If they will not connect directly, this method connects them with intervening transforms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de3adac7-ff99-4415-9afc-e25ad420df59">Render</a>
</td>
<td align="left" width="63%">
Adds a chain of filters to a specified output pin to render it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">RenderFile</a>
</td>
<td align="left" width="63%">
Builds a filter graph that renders the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/194960ee-3418-420f-9242-a372097e4dc9">SetLogFile</a>
</td>
<td align="left" width="63%">
Sets the file for logging actions taken when attempting to perform an operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d862a41-6896-40a5-8bfc-129b15dfc671">ShouldOperationContinue</a>
</td>
<td align="left" width="63%">
Queries whether the current operation should continue.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph</a>



<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

