---
UID: NE:searchapi.__MIDL___MIDL_itf_searchapi_0000_0013_0001
title: "__MIDL___MIDL_itf_searchapi_0000_0013_0001"
author: windows-sdk-content
description: These flags enumerate reasons why URLs are included or excluded from the current crawl scope.
old-location: search\_search_CLUSION_REASON.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\clusion_reason.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CLUSIONREASON_DEFAULT, CLUSIONREASON_GROUPPOLICY, CLUSIONREASON_UNKNOWNSCOPE, CLUSIONREASON_USER, CLUSION_REASON, CLUSION_REASON enumeration [search], __MIDL___MIDL_itf_searchapi_0000_0013_0001, _search_CLUSION_REASON, search._search_CLUSION_REASON, searchapi/CLUSIONREASON_DEFAULT, searchapi/CLUSIONREASON_GROUPPOLICY, searchapi/CLUSIONREASON_UNKNOWNSCOPE, searchapi/CLUSIONREASON_USER, searchapi/CLUSION_REASON
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
req.idl: Searchcrawlscopemanager.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CLUSION_REASON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Searchapi.h
api_name:
-	CLUSION_REASON
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_searchapi_0000_0013_0001 enumeration


## -description


These flags enumerate reasons why URLs are included or excluded from the current crawl scope. The 
<a href="https://msdn.microsoft.com/018c240b-491c-4974-8059-ee7331672e6b">ISearchCrawlScopeManager::IncludedInCrawlScopeEx</a> method returns a pointer to this enumeration to explain why a specified URL is either included or excluded from the current crawl scope.


## -enum-fields




### -field CLUSIONREASON_UNKNOWNSCOPE

The URL has been excluded because its scope in unknown. There is no scope that would include or exclude this URL so it is excluded by default.


### -field CLUSIONREASON_DEFAULT

The URL has been included or excluded by a default rule. Default rules are set during setup or first run.


### -field CLUSIONREASON_USER

The URL has been included or excluded by a user rule. User rules are set either by the user through Control Panel or by a calling application through the <a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a> interface.


### -field CLUSIONREASON_GROUPPOLICY

 Not Supported.

