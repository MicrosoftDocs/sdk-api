---
UID: NN:strmif.IFilterGraph2
title: IFilterGraph2
author: windows-sdk-content
description: The IFilterGraph2 interface extends the IFilterGraph and IGraphBuilder interfaces, which contain methods for building filter graphs.The Filter Graph Manager implements this interface.
old-location: dshow\ifiltergraph2.htm
tech.root: DirectShow
ms.assetid: 1a1ef4fe-a054-4ba7-99c7-1f209472c5a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFilterGraph2, IFilterGraph2 interface [DirectShow], IFilterGraph2 interface [DirectShow],described, IFilterGraph2Interface, dshow.ifiltergraph2, strmif/IFilterGraph2
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
 - IFilterGraph2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFilterGraph2 interface


## -description



The <code>IFilterGraph2</code> interface extends the <a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph</a> and <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interfaces, which contain methods for building filter graphs.

The Filter Graph Manager implements this interface. Applications can use it when building graphs, to take advantage of the additional methods it provides.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterGraph2</b> interface inherits from <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a>. <b>IFilterGraph2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterGraph2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e398df6-7cb7-4028-be34-3040a2cd1c2b">AddSourceFilterForMoniker</a>
</td>
<td align="left" width="63%">
Creates a source filter from a moniker and adds it to the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a72cf427-056b-4751-9c4a-665251e549f8">ReconnectEx</a>
</td>
<td align="left" width="63%">
Breaks an existing pin connection and reconnects the same pins, using a specified media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b169c784-2ce3-47dc-ad64-3e4c96483f34">RenderEx</a>
</td>
<td align="left" width="63%">
Renders an output pin, with an option to use existing renderers only.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a>
 

 

