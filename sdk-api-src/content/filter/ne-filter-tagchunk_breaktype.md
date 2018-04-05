---
UID: NE:filter.tagCHUNK_BREAKTYPE
title: tagCHUNK_BREAKTYPE
author: windows-driver-content
description: Describes the type of break that separates the current chunk from the previous chunk.
old-location: indexsrv\chunk_breaktype.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_9u1x.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: CHUNK_BREAKTYPE, CHUNK_BREAKTYPE enumeration [Indexing Service], CHUNK_EOC, CHUNK_EOP, CHUNK_EOS, CHUNK_EOW, CHUNK_NO_BREAK, _idxs_CHUNK_BREAKTYPE, filter/CHUNK_BREAKTYPE, filter/CHUNK_EOC, filter/CHUNK_EOP, filter/CHUNK_EOS, filter/CHUNK_EOW, filter/CHUNK_NO_BREAK, indexsrv.chunk_breaktype, tagCHUNK_BREAKTYPE
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CHUNK_BREAKTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Filter.h
api_name:
-	CHUNK_BREAKTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# tagCHUNK_BREAKTYPE enumeration


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

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




<a href="https://msdn.microsoft.com/4d4f3150-deec-40b6-a945-b4cea241db8d">IFilter::GetChunk</a>



<a href="https://msdn.microsoft.com/fb3e432d-3c8b-4567-9dc3-c35961f100ff">STAT_CHUNK</a>
 

 

