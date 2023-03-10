---
UID: NF:searchapi.ISearchCrawlScopeManager.AddUserScopeRule
title: ISearchCrawlScopeManager::AddUserScopeRule (searchapi.h)
description: Adds a new crawl scope rule when the user creates a new rule or adds a URL to be indexed.
helpviewer_keywords: ["AddUserScopeRule","AddUserScopeRule method [search]","AddUserScopeRule method [search]","ISearchCrawlScopeManager interface","ISearchCrawlScopeManager interface [search]","AddUserScopeRule method","ISearchCrawlScopeManager.AddUserScopeRule","ISearchCrawlScopeManager::AddUserScopeRule","_search_ISearchCrawlScopeManager_AddUserScopeRule","search._search_ISearchCrawlScopeManager_AddUserScopeRule","searchapi/ISearchCrawlScopeManager::AddUserScopeRule"]
old-location: search\_search_ISearchCrawlScopeManager_AddUserScopeRule.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\adduserscoperule.htm
ms.date: 12/05/2018
ms.keywords: AddUserScopeRule, AddUserScopeRule method [search], AddUserScopeRule method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],AddUserScopeRule method, ISearchCrawlScopeManager.AddUserScopeRule, ISearchCrawlScopeManager::AddUserScopeRule, _search_ISearchCrawlScopeManager_AddUserScopeRule, search._search_ISearchCrawlScopeManager_AddUserScopeRule, searchapi/ISearchCrawlScopeManager::AddUserScopeRule
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ISearchCrawlScopeManager::AddUserScopeRule
 - searchapi/ISearchCrawlScopeManager::AddUserScopeRule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchCrawlScopeManager.AddUserScopeRule
---

# ISearchCrawlScopeManager::AddUserScopeRule


## -description

Adds a new crawl scope rule when the user creates a new rule or adds a URL to be indexed.

## -parameters

### -param pszURL [in]

Type: <b>LPCWSTR</b>

The URL to be indexed.

### -param fInclude [in]

Type: <b>BOOL</b>

<b>TRUE</b> if this should be included in all <i>pszUrl</i> searches; otherwise, <b>FALSE</b>.

### -param fOverrideChildren [in]

Type: <b>BOOL</b>

A <b>BOOL</b> value specifying whether child rules should be overridden. If set to <b>TRUE</b>, this essentially removes all child rules.

### -param fFollowFlags [in]

Type: <b>DWORD</b>

Sets the <a href="/windows/desktop/api/searchapi/ne-searchapi-follow_flags">FOLLOW_FLAGS</a> to specify whether to follow complex URLs and whether a URL is to be indexed or just followed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A scope rule can be a fully qualified URL or a rule with a pattern.

<b>ISearchCrawlScopeManager::AddUserScopeRule</b> overrides any existing scope rule for the URL or pattern.

URLs passed in as parameters to <b>ISearchCrawlScopeManager::AddUserScopeRule</b> are expected to be fully URL-decoded and without URL control codes. For example, file:///c:\My Documents is fully URL-decoded, whereas file:///c:\My%20Documents is not.

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.