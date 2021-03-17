---
UID: NS:filtereg._FILTERED_DATA_SOURCES
title: FILTERED_DATA_SOURCES (filtereg.h)
description: Specifies parameters for a Shell data source for which a filter is loaded.
helpviewer_keywords: ["FILTERED_DATA_SOURCES","FILTERED_DATA_SOURCES structure [search]","filtereg/FILTERED_DATA_SOURCES","search.filtered_data_sources"]
old-location: search\filtered_data_sources.htm
tech.root: search
ms.assetid: 5baae290-aead-4986-a7d4-0302931e0104
ms.date: 12/05/2018
ms.keywords: FILTERED_DATA_SOURCES, FILTERED_DATA_SOURCES structure [search], filtereg/FILTERED_DATA_SOURCES, search.filtered_data_sources
req.header: filtereg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Filtereg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FILTERED_DATA_SOURCES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILTERED_DATA_SOURCES
 - filtereg/_FILTERED_DATA_SOURCES
 - FILTERED_DATA_SOURCES
 - filtereg/FILTERED_DATA_SOURCES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - filtereg.h
api_name:
 - FILTERED_DATA_SOURCES
---

# FILTERED_DATA_SOURCES structure


## -description

Specifies parameters for a Shell data source for which a filter is loaded.

## -struct-fields

### -field pwcsExtension

Pointer to a buffer that contains a file name extension.

### -field pwcsMime

Pointer to a buffer that contains the name of a MIME type.

### -field pClsid

Pointer to a CLSID that identifies the content type.

### -field pwcsOverride

Not implemented.

## -remarks

A filter, also known as a filter handler, is an implementation of the <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface.

<b>FILTERED_DATA_SOURCES</b> can hold one file content identifier of each type. CLSIDs are always searched first, followed by the  file name extension, then MIME type, and finally the path.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/search/-search-ifilter-conceptual">Developing Filter Handlers</a>



<a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>



<a href="/windows/desktop/api/filtereg/nn-filtereg-iloadfilter">ILoadFilter</a>



<b>Reference</b>