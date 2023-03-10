---
UID: NE:filter.tagCHUNKSTATE
title: CHUNKSTATE (filter.h)
description: Specifies whether the current chunk is a text-type property or a value-type property.
helpviewer_keywords: ["CHUNKSTATE","CHUNKSTATE enumeration [Indexing Service]","CHUNK_FILTER_OWNED_VALUE","CHUNK_TEXT","CHUNK_VALUE","_idxs_CHUNKSTATE","filter/CHUNKSTATE","filter/CHUNK_FILTER_OWNED_VALUE","filter/CHUNK_TEXT","filter/CHUNK_VALUE","indexsrv.chunkstate","tagCHUNKSTATE"]
old-location: indexsrv\chunkstate.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_6mat.htm
ms.date: 12/05/2018
ms.keywords: CHUNKSTATE, CHUNKSTATE enumeration [Indexing Service], CHUNK_FILTER_OWNED_VALUE, CHUNK_TEXT, CHUNK_VALUE, _idxs_CHUNKSTATE, filter/CHUNKSTATE, filter/CHUNK_FILTER_OWNED_VALUE, filter/CHUNK_TEXT, filter/CHUNK_VALUE, indexsrv.chunkstate, tagCHUNKSTATE
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
req.typenames: CHUNKSTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCHUNKSTATE
 - filter/tagCHUNKSTATE
 - CHUNKSTATE
 - filter/CHUNKSTATE
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
 - CHUNKSTATE
---

# CHUNKSTATE enumeration


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Specifies whether the current chunk is a text-type property or a value-type property.

## -enum-fields

### -field CHUNK_TEXT:0x1

The current chunk is a text-type property.

### -field CHUNK_VALUE:0x2

The current chunk is a value-type property.

### -field CHUNK_FILTER_OWNED_VALUE:0x4

Reserved.

## -see-also

<a href="/windows/desktop/api/filter/nf-filter-ifilter-getchunk">IFilter::GetChunk</a>



<a href="/windows/desktop/api/filter/nf-filter-ifilter-gettext">IFilter::GetText</a>



<a href="/windows/desktop/api/filter/ns-filter-stat_chunk">STAT_CHUNK</a>
