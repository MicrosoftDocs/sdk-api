---
UID: NE:filter.tagCHUNK_BREAKTYPE
title: CHUNK_BREAKTYPE (filter.h)
description: Describes the type of break that separates the current chunk from the previous chunk.helpviewer_keywords: ["CHUNK_BREAKTYPE","CHUNK_BREAKTYPE enumeration [Indexing Service]","CHUNK_EOC","CHUNK_EOP","CHUNK_EOS","CHUNK_EOW","CHUNK_NO_BREAK","_idxs_CHUNK_BREAKTYPE","filter/CHUNK_BREAKTYPE","filter/CHUNK_EOC","filter/CHUNK_EOP","filter/CHUNK_EOS","filter/CHUNK_EOW","filter/CHUNK_NO_BREAK","indexsrv.chunk_breaktype","tagCHUNK_BREAKTYPE"]
old-location: indexsrv\chunk_breaktype.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_9u1x.htm
ms.date: 12/05/2018
ms.keywords: CHUNK_BREAKTYPE, CHUNK_BREAKTYPE enumeration [Indexing Service], CHUNK_EOC, CHUNK_EOP, CHUNK_EOS, CHUNK_EOW, CHUNK_NO_BREAK, _idxs_CHUNK_BREAKTYPE, filter/CHUNK_BREAKTYPE, filter/CHUNK_EOC, filter/CHUNK_EOP, filter/CHUNK_EOS, filter/CHUNK_EOW, filter/CHUNK_NO_BREAK, indexsrv.chunk_breaktype, tagCHUNK_BREAKTYPE
f1_keywords:
- filter/CHUNK_BREAKTYPE
dev_langs:
- c++
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
- CHUNK_BREAKTYPE
targetos: Windows
req.typenames: CHUNK_BREAKTYPE
req.redist: 
ms.custom: 19H1
---

# CHUNK_BREAKTYPE enumeration


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="https://www.microsoft.com/download/details.aspx?id=18914">Microsoft Search Server Express</a> for server side search.]

Describes the type of break that separates the current chunk from the previous chunk. 


## -enum-fields




### -field CHUNK_NO_BREAK

No break is placed between the current chunk and the previous chunk. The chunks are glued together.


### -field CHUNK_EOW

A word break is placed between this chunk and the previous chunk that had the same attribute. Use of CHUNK_EOW should be minimized because the choice of word breaks is language-dependent, so determining word breaks is best left to the search engine.


### -field CHUNK_EOS

A sentence break is placed between this chunk and the previous chunk that had the same attribute.


### -field CHUNK_EOP

A paragraph break is placed between this chunk and the previous chunk that had the same attribute. 



### -field CHUNK_EOC

A chapter break is placed between this chunk and the previous chunk that had the same attribute.


## -remarks



A change in attributes implies a word, sentence, paragraph, or chapter break.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/filter/nf-filter-ifilter-getchunk">IFilter::GetChunk</a>



<a href="https://docs.microsoft.com/windows/desktop/api/filter/ns-filter-stat_chunk">STAT_CHUNK</a>
 

 

