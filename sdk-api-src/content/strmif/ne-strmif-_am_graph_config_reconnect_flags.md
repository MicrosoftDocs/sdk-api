---
UID: NE:strmif._AM_GRAPH_CONFIG_RECONNECT_FLAGS
title: "_AM_GRAPH_CONFIG_RECONNECT_FLAGS"
author: windows-sdk-content
description: Specifies how to reconnect filters when dynamically rebuilding the filter graph.
old-location: dshow\am_graph_config_reconnect_flags.htm
old-project: DirectShow
ms.assetid: 59f47597-3270-48b3-b927-09b434373eac
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: AM_GRAPH_CONFIG_RECONNECT_CACHE_REMOVED_FILTERS, AM_GRAPH_CONFIG_RECONNECT_DIRECTCONNECT, AM_GRAPH_CONFIG_RECONNECT_FLAGS, AM_GRAPH_CONFIG_RECONNECT_FLAGS , AM_GRAPH_CONFIG_RECONNECT_FLAGS enumeration [DirectShow], AM_GRAPH_CONFIG_RECONNECT_FLAGSEnumeration, AM_GRAPH_CONFIG_RECONNECT_USE_ONLY_CACHED_FILTERS, _AM_GRAPH_CONFIG_RECONNECT_FLAGS, dshow.am_graph_config_reconnect_flags, strmif/AM_GRAPH_CONFIG_RECONNECT_CACHE_REMOVED_FILTERS, strmif/AM_GRAPH_CONFIG_RECONNECT_DIRECTCONNECT, strmif/AM_GRAPH_CONFIG_RECONNECT_FLAGS, strmif/AM_GRAPH_CONFIG_RECONNECT_USE_ONLY_CACHED_FILTERS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: AM_GRAPH_CONFIG_RECONNECT_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	AM_GRAPH_CONFIG_RECONNECT_FLAGS
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1
---

# _AM_GRAPH_CONFIG_RECONNECT_FLAGS enumeration


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




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/e8cfac8e-df89-444d-bcc7-0cbc7ab5a592">IGraphConfig::Reconnect</a>



<a href="https://msdn.microsoft.com/9bcd325d-41fc-4166-8fce-50fc921efdba">IPinFlowControl::Block</a>
 

 

