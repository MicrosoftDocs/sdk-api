---
UID: NS:strmif._FilterInfo
title: FILTER_INFO (strmif.h)
description: The FILTER_INFO structure contains information about a filter.
helpviewer_keywords: ["FILTER_INFO","FILTER_INFO structure [DirectShow]","FILTER_INFOStructure","dshow.filter_info","strmif/FILTER_INFO"]
old-location: dshow\filter_info.htm
tech.root: dshow
ms.assetid: 43d1951e-448d-4139-879b-3fe021490d7d
ms.date: 12/05/2018
ms.keywords: FILTER_INFO, FILTER_INFO structure [DirectShow], FILTER_INFOStructure, dshow.filter_info, strmif/FILTER_INFO
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
req.typenames: FILTER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FilterInfo
 - strmif/_FilterInfo
 - FILTER_INFO
 - strmif/FILTER_INFO
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
 - FILTER_INFO
---

# FILTER_INFO structure


## -description

The <code>FILTER_INFO</code> structure contains information about a filter.

## -struct-fields

### -field achName

Null-terminated string containing the name of the filter.

### -field pGraph

If the filter is member of a filter graph, contains a pointer to the filter graph's <a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> interface. If the filter is not a member of a filter graph, this value of this member is <b>NULL</b>.

## -remarks

If the <b>pGraph</b> member is not <b>NULL</b>, the application should release the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> interface when it is finished using it.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>