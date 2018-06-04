---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

