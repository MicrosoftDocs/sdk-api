---
UID: NN:strmif.IGraphConfig
title: IGraphConfig (strmif.h)
author: windows-sdk-content
description: The Filter Graph Manager exposes IGraphConfig to support dynamic graph building.
old-location: dshow\igraphconfig.htm
tech.root: DirectShow
ms.assetid: 7df22157-9dd1-410e-b037-a155f7b9a01b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGraphConfig, IGraphConfig interface [DirectShow], IGraphConfig interface [DirectShow],described, IGraphConfigInterface, dshow.igraphconfig, strmif/IGraphConfig
ms.topic: interface
f1_keywords: 
 - "strmif/IGraphConfig"
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
ms.custom: 19H1
---

# IGraphConfig interface


## -description



The Filter Graph Manager exposes <code>IGraphConfig</code> to support dynamic graph building. This interface enables applications and filters to reconfigure the filter graph while the graph is in a running state, and without losing data from the stream.

The most straightforward way to rebuild the graph dynamically is to call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconnect">IGraphConfig::Reconnect</a> method. This method handles most of the details of dynamically rebuilding the graph. If a situation ever arises where you want to implement your own technique, <code>IGraphConfig</code> also provides the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconfigure">IGraphConfig::Reconfigure</a> method. This method obtains a lock on the filter graph and then calls a callback function in your application, which reconfigures the graph. With this method, most of the work is shifted to your application. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dynamic-graph-building">Dynamic Graph Building</a>.

To optimize the process of adding and removing filters, the filter graph maintains a cache of filters. During a call to the <b>Reconnect</b> method, you can specify that any filters removed from the graph get added to the cache. You can also add a filter to the cache directly, if you know it is likely to be needed, by calling <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-addfiltertocache">IGraphConfig::AddFilterToCache</a>. The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-render">IGraphBuilder::Render</a>, <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-connect">IGraphBuilder::Connect</a> methods automatically try to use filters in the cache before using other filters. Also, in the <b>Reconnect</b> method you can specify that only cached filters will be used for the reconnection. Note that filters held in the cache are not actually part of the graph. They are disconnected from any pins and are kept in a stopped state.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGraphConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGraphConfig</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-addfiltertocache">AddFilterToCache</a>
</td>
<td align="left" width="63%">
Adds a filter to the filter cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-enumcachefilter">EnumCacheFilter</a>
</td>
<td align="left" width="63%">
Enumerates the filters in the filter cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-getfilterflags">GetFilterFlags</a>
</td>
<td align="left" width="63%">
Retrieves a filter's configuration information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-getstarttime">GetStartTime</a>
</td>
<td align="left" width="63%">
Retrieves the reference time used when the filter graph was last put into a running state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-pushthroughdata">PushThroughData</a>
</td>
<td align="left" width="63%">
Pushes data through the filter graph to the specified pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconfigure">Reconfigure</a>
</td>
<td align="left" width="63%">
Locks the filter graph and calls a callback function in the application or filter to perform a dynamic reconfiguration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconnect">Reconnect</a>
</td>
<td align="left" width="63%">
Performs a dynamic reconnection between two pins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-removefilterex">RemoveFilterEx</a>
</td>
<td align="left" width="63%">
Removes a filter from the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-removefilterfromcache">RemoveFilterFromCache</a>
</td>
<td align="left" width="63%">
Removes a filter from the filter cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-setfilterflags">SetFilterFlags</a>
</td>
<td align="left" width="63%">
Sets a filter's configuration information.

</td>
</tr>
</table> 

