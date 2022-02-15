---
UID: NE:searchapi._FOLLOW_FLAGS
title: FOLLOW_FLAGS (searchapi.h)
description: Used to help define behavior when crawling or indexing. These flags are used by the ISearchCrawlScopeManager::AddDefaultScopeRule and ISearchCrawlScopeManager::AddUserScopeRule methods.
helpviewer_keywords: ["FF_INDEXCOMPLEXURLS","FF_SUPPRESSINDEXING","FOLLOW_FLAGS","FOLLOW_FLAGS enumeration [search]","_search_FOLLOW_FLAGS","search._search_FOLLOW_FLAGS","searchapi/FF_INDEXCOMPLEXURLS","searchapi/FF_SUPPRESSINDEXING","searchapi/FOLLOW_FLAGS"]
old-location: search\_search_FOLLOW_FLAGS.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\follow_flags.htm
ms.date: 12/05/2018
ms.keywords: FF_INDEXCOMPLEXURLS, FF_SUPPRESSINDEXING, FOLLOW_FLAGS, FOLLOW_FLAGS enumeration [search], _search_FOLLOW_FLAGS, search._search_FOLLOW_FLAGS, searchapi/FF_INDEXCOMPLEXURLS, searchapi/FF_SUPPRESSINDEXING, searchapi/FOLLOW_FLAGS
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcrawlscopemanager.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FOLLOW_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FOLLOW_FLAGS
 - searchapi/_FOLLOW_FLAGS
 - FOLLOW_FLAGS
 - searchapi/FOLLOW_FLAGS
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
 - FOLLOW_FLAGS
---

# FOLLOW_FLAGS enumeration


## -description

Used to help define behavior when crawling or indexing.  These flags are used by the <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule">ISearchCrawlScopeManager::AddDefaultScopeRule</a> and
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule">ISearchCrawlScopeManager::AddUserScopeRule</a> methods.

## -enum-fields

### -field FF_INDEXCOMPLEXURLS:0x1

Specifies whether complex URLs (those containing a '?') should be indexed.

### -field FF_SUPPRESSINDEXING:0x2

Follow but do not index this URL.
