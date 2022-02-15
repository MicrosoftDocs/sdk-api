---
UID: NE:strmif._FilterState
title: FILTER_STATE (strmif.h)
description: Specifies a filter's state or the state of the filter graph.
helpviewer_keywords: ["FILTER_STATE","FILTER_STATE","FILTER_STATE enumeration [DirectShow]","FILTER_STATEEnumeration","State_Paused","State_Running","State_Stopped","dshow.filter_state","strmif/FILTER_STATE","strmif/State_Paused","strmif/State_Running","strmif/State_Stopped"]
old-location: dshow\filter_state.htm
tech.root: dshow
ms.assetid: 41f88abc-57d1-4f80-a099-d17e624ab8a6
ms.date: 12/05/2018
ms.keywords: FILTER_STATE, FILTER_STATE , FILTER_STATE enumeration [DirectShow], FILTER_STATEEnumeration, State_Paused, State_Running, State_Stopped, dshow.filter_state, strmif/FILTER_STATE, strmif/State_Paused, strmif/State_Running, strmif/State_Stopped
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
req.typenames: FILTER_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FilterState
 - strmif/_FilterState
 - FILTER_STATE
 - strmif/FILTER_STATE
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
 - FILTER_STATE
---

# FILTER_STATE enumeration


## -description

Specifies a filter's state or the state of the filter graph.

## -enum-fields

### -field State_Stopped:0

Stopped. The filter is not processing data.

### -field State_Paused

Paused. The filter is processing data, but not rendering it.

### -field State_Running

Running. The filter is processing and rendering data.

## -see-also

<a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/control/nf-control-imediacontrol-getstate">IMediaControl::GetState</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediafilter-getstate">IMediaFilter::GetState</a>
