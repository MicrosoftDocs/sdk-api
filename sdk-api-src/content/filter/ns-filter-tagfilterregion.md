---
UID: NS:filter.tagFILTERREGION
title: tagFILTERREGION
author: windows-sdk-content
description: Describes the position and extent of a specified portion of text within an object. This structure is used by the IFilter::BindRegion method.
old-location: search\_search_FILTERREGION.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\filterregion.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FILTERREGION, FILTERREGION structure [search], _search_FILTERREGION, filter/FILTERREGION, search._search_FILTERREGION, tagFILTERREGION
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
req.redist: the Windows NT 4.0 Option Pack
---

# tagFILTERREGION structure


## -description


Describes the position and extent of a specified portion of text within an object. This structure is used by the <a href="https://msdn.microsoft.com/7654292f-1a77-48b6-af74-262cac4e111c">IFilter::BindRegion</a> method.


## -struct-fields




### -field idChunk

Type: <b>ULONG</b>

Chunk ID.


### -field cwcStart

Type: <b>ULONG</b>

Beginning of the region, specified as an offset from the beginning of the chunk.


### -field cwcExtent

Type: <b>ULONG</b>

Extent of the region, specified as a number of Unicode characters.


## -remarks



The <b>cwcExtent</b> member might specify a number of characters (starting from a position the <b>cwcStart</b> member specifies) that extends beyond the end of the chunk. In that case, the region should be continued into the next chunk, which should have the same attribute as the current region.




## -see-also




<a href="https://msdn.microsoft.com/7654292f-1a77-48b6-af74-262cac4e111c">IFilter::BindRegion</a>
 

 

