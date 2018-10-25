---
UID: NE:filter.tagCHUNK_BREAKTYPE
title: tagCHUNK_BREAKTYPE
author: windows-sdk-content
description: Describes the type of break that separates the current chunk from the previous chunk.
old-location: search\_search_CHUNK_BREAKTYPE.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\chunk_breaktype.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CHUNK_BREAKTYPE, CHUNK_BREAKTYPE enumeration [search], CHUNK_EOC, CHUNK_EOP, CHUNK_EOS, CHUNK_EOW, CHUNK_NO_BREAK, _search_CHUNK_BREAKTYPE, filter/CHUNK_BREAKTYPE, filter/CHUNK_EOC, filter/CHUNK_EOP, filter/CHUNK_EOS, filter/CHUNK_EOW, filter/CHUNK_NO_BREAK, search._search_CHUNK_BREAKTYPE, tagCHUNK_BREAKTYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: CHUNK_BREAKTYPE
req.redist: the Windows NT 4.0 Option Pack
---

# tagCHUNK_BREAKTYPE enumeration


## -description


Describes the type of break that separates the current chunk from the previous chunk.


## -enum-fields




### -field CHUNK_NO_BREAK

No break is placed between the current chunk and the previous chunk. The chunks are glued together.


### -field CHUNK_EOW

A word break is placed between this chunk and the previous chunk having the same attribute. Use of CHUNK_EOW should be minimized because the choice of word breaks is language-dependent, so determining word breaks is best left to the search engine.


### -field CHUNK_EOS

A sentence break is placed between this chunk and the previous chunk having the same attribute.


### -field CHUNK_EOP

A paragraph break is placed between this chunk and the previous chunk having the same attribute.


### -field CHUNK_EOC

A chapter break is placed between this chunk and the previous chunk having the same attribute.


## -remarks



A change in attributes implies a word, sentence, paragraph, or chapter break.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/361b0edc-579f-471a-8b4d-4ef1ae242b32">GetChunk</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/199e23f9-3cf8-48ba-8ad3-8122429c1640">STAT_CHUNK</a>



<a href="https://msdn.microsoft.com/cfba12eb-4123-4b57-8311-d4fc8f9f514e">The Indexing Process</a>
 

 

