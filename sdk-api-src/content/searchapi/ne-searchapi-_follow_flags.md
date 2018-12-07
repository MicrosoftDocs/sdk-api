---
UID: NE:searchapi._FOLLOW_FLAGS
title: "_FOLLOW_FLAGS"
author: windows-sdk-content
description: Used to help define behavior when crawling or indexing. These flags are used by the ISearchCrawlScopeManager::AddDefaultScopeRule and ISearchCrawlScopeManager::AddUserScopeRule methods.
old-location: search\_search_FOLLOW_FLAGS.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\follow_flags.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FF_INDEXCOMPLEXURLS, FF_SUPPRESSINDEXING, FOLLOW_FLAGS, FOLLOW_FLAGS enumeration [search], _FOLLOW_FLAGS, _search_FOLLOW_FLAGS, search._search_FOLLOW_FLAGS, searchapi/FF_INDEXCOMPLEXURLS, searchapi/FF_SUPPRESSINDEXING, searchapi/FOLLOW_FLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.idl: Searchcrawlscopemanager.idl
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
 - FOLLOW_FLAGS
product: Windows
targetos: Windows
req.typenames: FOLLOW_FLAGS
req.redist: 
---

# _FOLLOW_FLAGS enumeration


## -description


Used to help define behavior when crawling or indexing.  These flags are used by the <a href="https://msdn.microsoft.com/en-us/library/Bb266481(v=VS.85).aspx">ISearchCrawlScopeManager::AddDefaultScopeRule</a> and
<a href="https://msdn.microsoft.com/en-us/library/Bb266484(v=VS.85).aspx">ISearchCrawlScopeManager::AddUserScopeRule</a> methods.


## -enum-fields




### -field FF_INDEXCOMPLEXURLS

Specifies whether complex URLs (those containing a '?') should be indexed.


### -field FF_SUPPRESSINDEXING

Follow but do not index this URL.

