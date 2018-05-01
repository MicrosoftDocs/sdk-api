---
UID: NF:searchapi.ISearchCrawlScopeManager.AddUserScopeRule
title: ISearchCrawlScopeManager::AddUserScopeRule method
author: windows-driver-content
description: Adds a new crawl scope rule when the user creates a new rule or adds a URL to be indexed.
old-location: search\_search_ISearchCrawlScopeManager_AddUserScopeRule.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\adduserscoperule.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: AddUserScopeRule method [search], AddUserScopeRule method [search], ISearchCrawlScopeManager interface, AddUserScopeRule,ISearchCrawlScopeManager.AddUserScopeRule, ISearchCrawlScopeManager, ISearchCrawlScopeManager interface [search], AddUserScopeRule method, ISearchCrawlScopeManager::AddUserScopeRule, _search_ISearchCrawlScopeManager_AddUserScopeRule, search._search_ISearchCrawlScopeManager_AddUserScopeRule, searchapi/ISearchCrawlScopeManager::AddUserScopeRule
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchCrawlScopeManager.AddUserScopeRule
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchCrawlScopeManager::AddUserScopeRule method


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

Sets the <a href="https://msdn.microsoft.com/5890ffd2-5dbf-458b-9f40-d1df45648702">FOLLOW_FLAGS</a> to specify whether to follow complex URLs and whether a URL is to be indexed or just followed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A scope rule can be a fully qualified URL or a rule with a pattern.

<b>ISearchCrawlScopeManager::AddUserScopeRule</b> overrides any existing scope rule for the URL or pattern.

URLs passed in as parameters to <b>ISearchCrawlScopeManager::AddUserScopeRule</b> are expected to be fully URL-decoded and without URL control codes. For example, file:///c:\My Documents is fully URL-decoded, whereas file:///c:\My%20Documents is not.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



