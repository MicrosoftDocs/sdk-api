---
UID: NE:searchapi._SEARCH_TERM_EXPANSION
title: "_SEARCH_TERM_EXPANSION"
author: windows-sdk-content
description: Indicates wildcard options on search terms. Used by ISearchQueryHelper::get_QueryTermExpansion and ISearchQueryHelper::put_QueryTermExpansion methods.
old-location: search\_search_SEARCH_TERM_EXPANSION.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\search_term_expansion.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: SEARCH_TERM_EXPANSION, SEARCH_TERM_EXPANSION enumeration [search], SEARCH_TERM_NO_EXPANSION, SEARCH_TERM_PREFIX_ALL, SEARCH_TERM_STEM_ALL, _SEARCH_TERM_EXPANSION, _search_SEARCH_TERM_EXPANSION, search._search_SEARCH_TERM_EXPANSION, searchapi/SEARCH_TERM_EXPANSION, searchapi/SEARCH_TERM_NO_EXPANSION, searchapi/SEARCH_TERM_PREFIX_ALL, searchapi/SEARCH_TERM_STEM_ALL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Searchapi.h
api_name:
 - SEARCH_TERM_EXPANSION
product: Windows
targetos: Windows
req.typenames: SEARCH_TERM_EXPANSION
req.redist: Windows Desktop Search (WDS) 3.0
---

# _SEARCH_TERM_EXPANSION enumeration


## -description


Indicates wildcard options on search terms. Used by <a href="https://msdn.microsoft.com/3af83c74-e2af-40f1-afdd-fec286b42be2">ISearchQueryHelper::get_QueryTermExpansion</a> and <a href="https://msdn.microsoft.com/edcc8a86-b677-4f84-aa6f-90ada895dbcc">ISearchQueryHelper::put_QueryTermExpansion</a> methods.


## -enum-fields




### -field SEARCH_TERM_NO_EXPANSION

No expansion is applied to search terms.


### -field SEARCH_TERM_PREFIX_ALL

All search terms are expanded.


### -field SEARCH_TERM_STEM_ALL

Stem expansion is applied to all terms.


## -remarks



While the <b>SEARCH_TERM_EXPANSION</b> enumerated type lets you specify stem expansion, Windows Search does not currently support its use with the <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a> interface.



