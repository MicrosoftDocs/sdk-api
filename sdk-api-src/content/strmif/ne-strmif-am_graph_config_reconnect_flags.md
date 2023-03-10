---
UID: NE:strmif._AM_GRAPH_CONFIG_RECONNECT_FLAGS
title: AM_GRAPH_CONFIG_RECONNECT_FLAGS (strmif.h)
description: Specifies how to reconnect filters when dynamically rebuilding the filter graph.
helpviewer_keywords: ["AM_GRAPH_CONFIG_RECONNECT_CACHE_REMOVED_FILTERS","AM_GRAPH_CONFIG_RECONNECT_DIRECTCONNECT","AM_GRAPH_CONFIG_RECONNECT_FLAGS","AM_GRAPH_CONFIG_RECONNECT_FLAGS","AM_GRAPH_CONFIG_RECONNECT_FLAGS enumeration [DirectShow]","AM_GRAPH_CONFIG_RECONNECT_FLAGSEnumeration","AM_GRAPH_CONFIG_RECONNECT_USE_ONLY_CACHED_FILTERS","dshow.am_graph_config_reconnect_flags","strmif/AM_GRAPH_CONFIG_RECONNECT_CACHE_REMOVED_FILTERS","strmif/AM_GRAPH_CONFIG_RECONNECT_DIRECTCONNECT","strmif/AM_GRAPH_CONFIG_RECONNECT_FLAGS","strmif/AM_GRAPH_CONFIG_RECONNECT_USE_ONLY_CACHED_FILTERS"]
old-location: dshow\am_graph_config_reconnect_flags.htm
tech.root: dshow
ms.assetid: 59f47597-3270-48b3-b927-09b434373eac
ms.date: 12/05/2018
ms.keywords: AM_GRAPH_CONFIG_RECONNECT_CACHE_REMOVED_FILTERS, AM_GRAPH_CONFIG_RECONNECT_DIRECTCONNECT, AM_GRAPH_CONFIG_RECONNECT_FLAGS, AM_GRAPH_CONFIG_RECONNECT_FLAGS , AM_GRAPH_CONFIG_RECONNECT_FLAGS enumeration [DirectShow], AM_GRAPH_CONFIG_RECONNECT_FLAGSEnumeration, AM_GRAPH_CONFIG_RECONNECT_USE_ONLY_CACHED_FILTERS, dshow.am_graph_config_reconnect_flags, strmif/AM_GRAPH_CONFIG_RECONNECT_CACHE_REMOVED_FILTERS, strmif/AM_GRAPH_CONFIG_RECONNECT_DIRECTCONNECT, strmif/AM_GRAPH_CONFIG_RECONNECT_FLAGS, strmif/AM_GRAPH_CONFIG_RECONNECT_USE_ONLY_CACHED_FILTERS
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
targetos: Windows
req.typenames: AM_GRAPH_CONFIG_RECONNECT_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_GRAPH_CONFIG_RECONNECT_FLAGS
 - strmif/_AM_GRAPH_CONFIG_RECONNECT_FLAGS
 - AM_GRAPH_CONFIG_RECONNECT_FLAGS
 - strmif/AM_GRAPH_CONFIG_RECONNECT_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - AM_GRAPH_CONFIG_RECONNECT_FLAGS
---

# AM_GRAPH_CONFIG_RECONNECT_FLAGS enumeration


## -description

Specifies how to reconnect filters when dynamically rebuilding the filter graph.

## -enum-fields

### -field AM_GRAPH_CONFIG_RECONNECT_DIRECTCONNECT:0x1

Do not insert additional filters into the graph while reconnecting, aside from any filter explicitly requested.

### -field AM_GRAPH_CONFIG_RECONNECT_CACHE_REMOVED_FILTERS:0x2

Place filters removed from the graph into the filter cache.

### -field AM_GRAPH_CONFIG_RECONNECT_USE_ONLY_CACHED_FILTERS:0x4

When inserting additional filters into the graph, use only filters currently in the filter cache.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconnect">IGraphConfig::Reconnect</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ipinflowcontrol-block">IPinFlowControl::Block</a>
