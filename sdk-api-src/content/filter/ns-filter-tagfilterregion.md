---
UID: NS:filter.tagFILTERREGION
title: tagFILTERREGION
author: windows-sdk-content
description: Describes the position and extent of a specified portion of text within an object.
old-location: indexsrv\filterregion.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_9usu.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FILTERREGION, FILTERREGION structure [Indexing Service], _idxs_FILTERREGION, filter/FILTERREGION, indexsrv.filterregion, tagFILTERREGION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - FILTERREGION
product: Windows
targetos: Windows
req.typenames: FILTERREGION
req.redist: 
---

# tagFILTERREGION structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

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




<a href="https://msdn.microsoft.com/d4ee07f3-4260-4b33-9ac9-436d17c80f2c">IFilter::BindRegion</a>
 

 

