---
UID: NN:strmif.IFilterGraph
title: IFilterGraph
author: windows-sdk-content
description: The IFilterGraph interface provides methods for building a filter graph.
old-location: dshow\ifiltergraph.htm
tech.root: DirectShow
ms.assetid: 73a92f44-03c6-47e3-98d1-a20100ed8fa1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFilterGraph, IFilterGraph interface [DirectShow], IFilterGraph interface [DirectShow],described, IFilterGraphInterface, dshow.ifiltergraph, strmif/IFilterGraph
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
 - IFilterGraph
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFilterGraph interface


## -description



The <code>IFilterGraph</code> interface provides methods for building a filter graph. An application can use it to add filters to the graph, connect or disconnect filters, remove filters, and perform other basic operations. However, the <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface inherits from this interface and provides additional methods that are more sophisticated. Therefore, applications should use <b>IGraphBuilder</b> rather than using <code>IFilterGraph</code> directly.

The filter graph manager implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterGraph</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFilterGraph</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterGraph</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f837917-015f-427f-b234-b0ccbcf943eb">AddFilter</a>
</td>
<td align="left" width="63%">
Adds a filter to the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb17bd98-dd6b-4fad-9b56-9cab10725b28">ConnectDirect</a>
</td>
<td align="left" width="63%">
Connects two pins directly (without intervening filters).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c7d6cb6-b91c-4461-8f2b-38342a88eafc">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects a specified pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a6dcd1a-3ec3-4f0f-8e82-2d33ad775eec">EnumFilters</a>
</td>
<td align="left" width="63%">
Provides an enumerator for all filters in the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59d90274-ac00-4e19-bcee-2282e26994b5">FindFilterByName</a>
</td>
<td align="left" width="63%">
Finds a filter that was added with a specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98a46014-031b-4f35-b1bc-58aef411360b">Reconnect</a>
</td>
<td align="left" width="63%">
Breaks the existing pin connection and reconnects it to the same pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec681340-0fb9-4eba-8211-d5fa07fb076b">RemoveFilter</a>
</td>
<td align="left" width="63%">
Removes a filter from the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/775e7136-f6d0-47bc-852f-1c5c88ad03bf">SetDefaultSyncSource</a>
</td>
<td align="left" width="63%">
Sets the reference clock to the default clock.

</td>
</tr>
</table> 

