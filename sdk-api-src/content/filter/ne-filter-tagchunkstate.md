---
UID: NE:filter.tagCHUNKSTATE
title: tagCHUNKSTATE
author: windows-driver-content
description: Specifies whether the current chunk is a text-type property or a value-type property.
old-location: indexsrv\chunkstate.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_6mat.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: CHUNKSTATE, CHUNKSTATE enumeration [Indexing Service], CHUNK_FILTER_OWNED_VALUE, CHUNK_TEXT, CHUNK_VALUE, _idxs_CHUNKSTATE, filter/CHUNKSTATE, filter/CHUNK_FILTER_OWNED_VALUE, filter/CHUNK_TEXT, filter/CHUNK_VALUE, indexsrv.chunkstate, tagCHUNKSTATE
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
req.typenames: CHUNKSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Filter.h
api_name:
-	CHUNKSTATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# tagCHUNKSTATE enumeration


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Specifies whether the current chunk is a text-type property or a value-type property.



## -enum-fields




### -field CHUNK_TEXT

The current chunk is a text-type property.


### -field CHUNK_VALUE

The current chunk is a value-type property.


### -field CHUNK_FILTER_OWNED_VALUE

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/4d4f3150-deec-40b6-a945-b4cea241db8d">IFilter::GetChunk</a>



<a href="https://msdn.microsoft.com/d63639a6-6729-44cd-8105-198a268ff2d6">IFilter::GetText</a>



<a href="https://msdn.microsoft.com/fb3e432d-3c8b-4567-9dc3-c35961f100ff">STAT_CHUNK</a>
 

 

