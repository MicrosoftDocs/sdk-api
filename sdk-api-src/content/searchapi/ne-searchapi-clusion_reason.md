---
UID: NE:searchapi.__MIDL___MIDL_itf_searchapi_0000_0013_0001
title: CLUSION_REASON (searchapi.h)
description: These flags enumerate reasons why URLs are included or excluded from the current crawl scope.
helpviewer_keywords: ["CLUSIONREASON_DEFAULT","CLUSIONREASON_GROUPPOLICY","CLUSIONREASON_UNKNOWNSCOPE","CLUSIONREASON_USER","CLUSION_REASON","CLUSION_REASON enumeration [search]","_search_CLUSION_REASON","search._search_CLUSION_REASON","searchapi/CLUSIONREASON_DEFAULT","searchapi/CLUSIONREASON_GROUPPOLICY","searchapi/CLUSIONREASON_UNKNOWNSCOPE","searchapi/CLUSIONREASON_USER","searchapi/CLUSION_REASON"]
old-location: search\_search_CLUSION_REASON.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\clusion_reason.htm
ms.date: 12/05/2018
ms.keywords: CLUSIONREASON_DEFAULT, CLUSIONREASON_GROUPPOLICY, CLUSIONREASON_UNKNOWNSCOPE, CLUSIONREASON_USER, CLUSION_REASON, CLUSION_REASON enumeration [search], _search_CLUSION_REASON, search._search_CLUSION_REASON, searchapi/CLUSIONREASON_DEFAULT, searchapi/CLUSIONREASON_GROUPPOLICY, searchapi/CLUSIONREASON_UNKNOWNSCOPE, searchapi/CLUSIONREASON_USER, searchapi/CLUSION_REASON
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
req.typenames: CLUSION_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_searchapi_0000_0013_0001
 - searchapi/__MIDL___MIDL_itf_searchapi_0000_0013_0001
 - CLUSION_REASON
 - searchapi/CLUSION_REASON
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
 - CLUSION_REASON
---

# CLUSION_REASON enumeration


## -description

These flags enumerate reasons why URLs are included or excluded from the current crawl scope. The 
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex">ISearchCrawlScopeManager::IncludedInCrawlScopeEx</a> method returns a pointer to this enumeration to explain why a specified URL is either included or excluded from the current crawl scope.

## -enum-fields

### -field CLUSIONREASON_UNKNOWNSCOPE:0

The URL has been excluded because its scope in unknown. There is no scope that would include or exclude this URL so it is excluded by default.

### -field CLUSIONREASON_DEFAULT:1

The URL has been included or excluded by a default rule. Default rules are set during setup or first run.

### -field CLUSIONREASON_USER:2

The URL has been included or excluded by a user rule. User rules are set either by the user through Control Panel or by a calling application through the <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a> interface.

### -field CLUSIONREASON_GROUPPOLICY:3

 Not Supported.
