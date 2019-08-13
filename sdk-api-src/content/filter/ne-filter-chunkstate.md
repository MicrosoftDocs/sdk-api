---
UID: NE:filter.tagCHUNKSTATE
title: CHUNKSTATE (filter.h)
author: windows-sdk-content
description: Specifies whether the current chunk is a text-type property or a value-type property.
old-location: indexsrv\chunkstate.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_6mat.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CHUNKSTATE, CHUNKSTATE enumeration [Indexing Service], CHUNK_FILTER_OWNED_VALUE, CHUNK_TEXT, CHUNK_VALUE, _idxs_CHUNKSTATE, filter/CHUNKSTATE, filter/CHUNK_FILTER_OWNED_VALUE, filter/CHUNK_TEXT, filter/CHUNK_VALUE, indexsrv.chunkstate, tagCHUNKSTATE
ms.topic: enum
f1_keywords: 
 - "filter/CHUNKSTATE"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Filter.h
api_name:
 - CHUNKSTATE
product: Windows
targetos: Windows
req.typenames: CHUNKSTATE
req.redist: 
ms.custom: 19H1
---

# CHUNKSTATE enumeration


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Specifies whether the current chunk is a text-type property or a value-type property.



## -enum-fields




### -field CHUNK_TEXT

The current chunk is a text-type property.


### -field CHUNK_VALUE

The current chunk is a value-type property.


### -field CHUNK_FILTER_OWNED_VALUE

Reserved.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/filter/nf-filter-ifilter-getchunk">IFilter::GetChunk</a>



<a href="https://docs.microsoft.com/windows/desktop/api/filter/nf-filter-ifilter-gettext">IFilter::GetText</a>



<a href="https://docs.microsoft.com/windows/desktop/api/filter/ns-filter-stat_chunk">STAT_CHUNK</a>
 

 

