---
UID: NS:filter.tagFILTERREGION
title: FILTERREGION (filter.h)
description: Describes the position and extent of a specified portion of text within an object.
helpviewer_keywords: ["FILTERREGION","FILTERREGION structure [Indexing Service]","_idxs_FILTERREGION","filter/FILTERREGION","indexsrv.filterregion","tagFILTERREGION"]
old-location: indexsrv\filterregion.htm
tech.root: search
ms.assetid: VS|indexsrv|~\html\ixrefint_9usu.htm
ms.date: 12/05/2018
ms.keywords: FILTERREGION, FILTERREGION structure [Indexing Service], _idxs_FILTERREGION, filter/FILTERREGION, indexsrv.filterregion, tagFILTERREGION
req.header: filter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: FILTERREGION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFILTERREGION
 - filter/tagFILTERREGION
 - FILTERREGION
 - filter/FILTERREGION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Filter.h
api_name:
 - FILTERREGION
---

# FILTERREGION structure


## -description

Describes the position and extent of a specified portion of text within an object.

## -struct-fields

### -field idChunk

The chunk identifier.

### -field cwcStart

The beginning of the region, specified as an offset from the beginning of the chunk.

### -field cwcExtent

The extent of the region, specified as the number of Unicode characters.

## -remarks

The <b>cwcExtent</b> member might specify a number of characters (starting from a position the <b>cwcStart</b> member specifies) that extends beyond the end of the chunk. In that case, the region should be continued into the next chunk, which should have the same attribute as the current region.

## -see-also

<a href="/windows/desktop/api/filter/nf-filter-ifilter-bindregion">IFilter::BindRegion</a>