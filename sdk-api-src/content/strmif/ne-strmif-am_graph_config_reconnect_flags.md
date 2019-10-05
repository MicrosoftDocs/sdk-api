---
UID: NE:strmif._AM_GRAPH_CONFIG_RECONNECT_FLAGS
title: AM_GRAPH_CONFIG_RECONNECT_FLAGS (strmif.h)
author: windows-sdk-content
description: Specifies how to reconnect filters when dynamically rebuilding the filter graph.
old-location: dshow\am_graph_config_reconnect_flags.htm
tech.root: DirectShow
ms.assetid: 59f47597-3270-48b3-b927-09b434373eac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AM_GRAPH_CONFIG_RECONNECT_CACHE_REMOVED_FILTERS, AM_GRAPH_CONFIG_RECONNECT_DIRECTCONNECT, AM_GRAPH_CONFIG_RECONNECT_FLAGS, AM_GRAPH_CONFIG_RECONNECT_FLAGS , AM_GRAPH_CONFIG_RECONNECT_FLAGS enumeration [DirectShow], AM_GRAPH_CONFIG_RECONNECT_FLAGSEnumeration, AM_GRAPH_CONFIG_RECONNECT_USE_ONLY_CACHED_FILTERS, dshow.am_graph_config_reconnect_flags, strmif/AM_GRAPH_CONFIG_RECONNECT_CACHE_REMOVED_FILTERS, strmif/AM_GRAPH_CONFIG_RECONNECT_DIRECTCONNECT, strmif/AM_GRAPH_CONFIG_RECONNECT_FLAGS, strmif/AM_GRAPH_CONFIG_RECONNECT_USE_ONLY_CACHED_FILTERS
ms.topic: enum
f1_keywords: 
 - "strmif/AM_GRAPH_CONFIG_RECONNECT_FLAGS"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
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
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - AM_GRAPH_CONFIG_RECONNECT_FLAGS
targetos: Windows
req.typenames: AM_GRAPH_CONFIG_RECONNECT_FLAGS
req.redist: 
ms.custom: 19H1
---

# AM_GRAPH_CONFIG_RECONNECT_FLAGS enumeration


## -description



Specifies how to reconnect filters when dynamically rebuilding the filter graph.




## -enum-fields




### -field AM_GRAPH_CONFIG_RECONNECT_DIRECTCONNECT

Do not insert additional filters into the graph while reconnecting, aside from any filter explicitly requested.


### -field AM_GRAPH_CONFIG_RECONNECT_CACHE_REMOVED_FILTERS

Place filters removed from the graph into the filter cache.


### -field AM_GRAPH_CONFIG_RECONNECT_USE_ONLY_CACHED_FILTERS

When inserting additional filters into the graph, use only filters currently in the filter cache.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconnect">IGraphConfig::Reconnect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipinflowcontrol-block">IPinFlowControl::Block</a>
 

 

