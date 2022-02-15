---
UID: NE:searchapi._SEARCH_TERM_EXPANSION
title: SEARCH_TERM_EXPANSION (searchapi.h)
description: Indicates wildcard options on search terms. Used by ISearchQueryHelper::get_QueryTermExpansion and ISearchQueryHelper::put_QueryTermExpansion methods.
helpviewer_keywords: ["SEARCH_TERM_EXPANSION","SEARCH_TERM_EXPANSION enumeration [search]","SEARCH_TERM_NO_EXPANSION","SEARCH_TERM_PREFIX_ALL","SEARCH_TERM_STEM_ALL","_search_SEARCH_TERM_EXPANSION","search._search_SEARCH_TERM_EXPANSION","searchapi/SEARCH_TERM_EXPANSION","searchapi/SEARCH_TERM_NO_EXPANSION","searchapi/SEARCH_TERM_PREFIX_ALL","searchapi/SEARCH_TERM_STEM_ALL"]
old-location: search\_search_SEARCH_TERM_EXPANSION.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\search_term_expansion.htm
ms.date: 12/05/2018
ms.keywords: SEARCH_TERM_EXPANSION, SEARCH_TERM_EXPANSION enumeration [search], SEARCH_TERM_NO_EXPANSION, SEARCH_TERM_PREFIX_ALL, SEARCH_TERM_STEM_ALL, _search_SEARCH_TERM_EXPANSION, search._search_SEARCH_TERM_EXPANSION, searchapi/SEARCH_TERM_EXPANSION, searchapi/SEARCH_TERM_NO_EXPANSION, searchapi/SEARCH_TERM_PREFIX_ALL, searchapi/SEARCH_TERM_STEM_ALL
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
targetos: Windows
req.typenames: SEARCH_TERM_EXPANSION
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _SEARCH_TERM_EXPANSION
 - searchapi/_SEARCH_TERM_EXPANSION
 - SEARCH_TERM_EXPANSION
 - searchapi/SEARCH_TERM_EXPANSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - SEARCH_TERM_EXPANSION
---

# SEARCH_TERM_EXPANSION enumeration


## -description

Indicates wildcard options on search terms. Used by <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion">ISearchQueryHelper::get_QueryTermExpansion</a> and <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion">ISearchQueryHelper::put_QueryTermExpansion</a> methods.

## -enum-fields

### -field SEARCH_TERM_NO_EXPANSION:0

No expansion is applied to search terms.

### -field SEARCH_TERM_PREFIX_ALL

All search terms are expanded.

### -field SEARCH_TERM_STEM_ALL

Stem expansion is applied to all terms.

## -remarks

While the <b>SEARCH_TERM_EXPANSION</b> enumerated type lets you specify stem expansion, Windows Search does not currently support its use with the <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a> interface.
