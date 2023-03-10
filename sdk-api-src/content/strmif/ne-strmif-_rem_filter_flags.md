---
UID: NE:strmif._REM_FILTER_FLAGS
title: "_REM_FILTER_FLAGS (strmif.h)"
description: Specifies how to remove a filter from the filter graph.
helpviewer_keywords: ["REMFILTERF_LEAVECONNECTED","REM_FILTER_FLAGS","REM_FILTER_FLAGSEnumeration","_REM_FILTER_FLAGS","_REM_FILTER_FLAGS enumeration [DirectShow]","dshow.rem_filter_flags","strmif/REMFILTERF_LEAVECONNECTED","strmif/_REM_FILTER_FLAGS"]
old-location: dshow\rem_filter_flags.htm
tech.root: dshow
ms.assetid: 0bc91914-fa43-4ab7-a85e-30590a717c47
ms.date: 12/05/2018
ms.keywords: REMFILTERF_LEAVECONNECTED, REM_FILTER_FLAGS , REM_FILTER_FLAGSEnumeration, _REM_FILTER_FLAGS, _REM_FILTER_FLAGS enumeration [DirectShow], dshow.rem_filter_flags, strmif/REMFILTERF_LEAVECONNECTED, strmif/_REM_FILTER_FLAGS
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _REM_FILTER_FLAGS
 - strmif/_REM_FILTER_FLAGS
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
 - _REM_FILTER_FLAGS
---

# _REM_FILTER_FLAGS enumeration


## -description

Specifies how to remove a filter from the filter graph.

## -enum-fields

### -field REMFILTERF_LEAVECONNECTED:0x1

Leave the filter connected. By default, filters are disconnected when removed from the graph.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-removefilterex">IGraphConfig::RemoveFilterEx</a>
