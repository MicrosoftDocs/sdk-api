---
UID: NN:strmif.IGraphConfig
title: IGraphConfig
author: windows-sdk-content
description: The Filter Graph Manager exposes IGraphConfig to support dynamic graph building.
old-location: dshow\igraphconfig.htm
tech.root: DirectShow
ms.assetid: 7df22157-9dd1-410e-b037-a155f7b9a01b
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IGraphConfig, IGraphConfig interface [DirectShow], IGraphConfig interface [DirectShow],described, IGraphConfigInterface, dshow.igraphconfig, strmif/IGraphConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IGraphConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGraphConfig interface


## -description



The Filter Graph Manager exposes <code>IGraphConfig</code> to support dynamic graph building. This interface enables applications and filters to reconfigure the filter graph while the graph is in a running state, and without losing data from the stream.

The most straightforward way to rebuild the graph dynamically is to call the <a href="https://msdn.microsoft.com/e8cfac8e-df89-444d-bcc7-0cbc7ab5a592">IGraphConfig::Reconnect</a> method. This method handles most of the details of dynamically rebuilding the graph. If a situation ever arises where you want to implement your own technique, <code>IGraphConfig</code> also provides the <a href="https://msdn.microsoft.com/924087c0-e3ad-437b-96e5-de39bbce2ea7">IGraphConfig::Reconfigure</a> method. This method obtains a lock on the filter graph and then calls a callback function in your application, which reconfigures the graph. With this method, most of the work is shifted to your application. For more information, see <a href="https://msdn.microsoft.com/13fed430-979b-40f7-91ba-aff2d811bd92">Dynamic Graph Building</a>.

To optimize the process of adding and removing filters, the filter graph maintains a cache of filters. During a call to the <b>Reconnect</b> method, you can specify that any filters removed from the graph get added to the cache. You can also add a filter to the cache directly, if you know it is likely to be needed, by calling <a href="https://msdn.microsoft.com/8d5c6d55-1628-462b-828a-50541b6da3e7">IGraphConfig::AddFilterToCache</a>. The <a href="https://msdn.microsoft.com/de3adac7-ff99-4415-9afc-e25ad420df59">IGraphBuilder::Render</a>, <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a>, and <a href="https://msdn.microsoft.com/8ddcbb73-8220-4d70-9ab3-58d99fa8a958">IGraphBuilder::Connect</a> methods automatically try to use filters in the cache before using other filters. Also, in the <b>Reconnect</b> method you can specify that only cached filters will be used for the reconnection. Note that filters held in the cache are not actually part of the graph. They are disconnected from any pins and are kept in a stopped state.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGraphConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGraphConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGraphConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d5c6d55-1628-462b-828a-50541b6da3e7">AddFilterToCache</a>
</td>
<td align="left" width="63%">
Adds a filter to the filter cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1782def0-13ed-411c-ab05-d0f0c307e16a">EnumCacheFilter</a>
</td>
<td align="left" width="63%">
Enumerates the filters in the filter cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/747c3865-1969-45e8-a2c9-dbd72a9ea463">GetFilterFlags</a>
</td>
<td align="left" width="63%">
Retrieves a filter's configuration information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76d06517-3029-4ece-934e-b1c6f7f65f2c">GetStartTime</a>
</td>
<td align="left" width="63%">
Retrieves the reference time used when the filter graph was last put into a running state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3d72a32-f43a-4a61-b25e-6d472aa629de">PushThroughData</a>
</td>
<td align="left" width="63%">
Pushes data through the filter graph to the specified pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/924087c0-e3ad-437b-96e5-de39bbce2ea7">Reconfigure</a>
</td>
<td align="left" width="63%">
Locks the filter graph and calls a callback function in the application or filter to perform a dynamic reconfiguration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8cfac8e-df89-444d-bcc7-0cbc7ab5a592">Reconnect</a>
</td>
<td align="left" width="63%">
Performs a dynamic reconnection between two pins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3298aa2-4eb2-4e47-9f36-5f2cf541d13e">RemoveFilterEx</a>
</td>
<td align="left" width="63%">
Removes a filter from the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a23710d0-85aa-4ae0-84ea-03b9e22091ad">RemoveFilterFromCache</a>
</td>
<td align="left" width="63%">
Removes a filter from the filter cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f2ed50e-8bb9-4076-ad0e-a7311acb8285">SetFilterFlags</a>
</td>
<td align="left" width="63%">
Sets a filter's configuration information.

</td>
</tr>
</table> 

