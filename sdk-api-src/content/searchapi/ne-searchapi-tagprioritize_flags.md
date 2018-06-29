---
UID: NE:searchapi.tagPRIORITIZE_FLAGS
title: tagPRIORITIZE_FLAGS
author: windows-sdk-content
description: Used by PrioritizeMatchingURLs to specify how to process items the indexer has previously failed to index.
old-location: search\_search_PRIORITIZE_FLAGS.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\prioritize_flags.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PRIORITIZE_FLAGS, PRIORITIZE_FLAGS enumeration [search], PRIORITIZE_FLAG_IGNOREFAILURECOUNT, PRIORITIZE_FLAG_RETRYFAILEDITEMS, _search_PRIORITIZE_FLAGS, search._search_PRIORITIZE_FLAGS, searchapi/PRIORITIZE_FLAGS, searchapi/PRIORITIZE_FLAG_IGNOREFAILURECOUNT, searchapi/PRIORITIZE_FLAG_RETRYFAILEDITEMS, tagPRIORITIZE_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcatalog.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - PRIORITIZE_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: ADAM
---

# tagPRIORITIZE_FLAGS enumeration


## -description


Used by <a href="https://msdn.microsoft.com/library/Cc288278(v=VS.85).aspx">PrioritizeMatchingURLs</a> to specify how to process items the indexer has previously failed to index.


## -enum-fields




### -field PRIORITIZE_FLAG_RETRYFAILEDITEMS

Indicates that the indexer should reattempt to index items that it failed to index previously.


### -field PRIORITIZE_FLAG_IGNOREFAILURECOUNT

Indicates that the indexer should continue to reattempt indexing items regardless of the number of times the indexer has failed to index them previously.


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/Dd318747(v=VS.85).aspx">IRowsetPrioritization</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/library/Dd797839(v=VS.85).aspx">PRIORITY_LEVEL</a>



<a href="https://msdn.microsoft.com/library/Dd368861(v=VS.85).aspx">ROWSETEVENT_ITEMSTATE</a>



<a href="https://msdn.microsoft.com/library/Dd368862(v=VS.85).aspx">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Cc465173(v=VS.85).aspx">Rowset Properties</a>
 

 

