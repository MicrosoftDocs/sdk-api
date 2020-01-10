---
UID: NF:searchapi.ISearchScopeRule.get_IsDefault
title: ISearchScopeRule::get_IsDefault (searchapi.h)
description: Gets a value that identifies whether this is a default rule.
old-location: search\_search_ISearchScopeRule_get_IsDefault.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchscoperule\get_isdefault.htm
ms.date: 12/05/2018
ms.keywords: ISearchScopeRule interface [search],get_IsDefault method, ISearchScopeRule.get_IsDefault, ISearchScopeRule::get_IsDefault, _search_ISearchScopeRule_get_IsDefault, get_IsDefault, get_IsDefault method [search], get_IsDefault method [search],ISearchScopeRule interface, search._search_ISearchScopeRule_get_IsDefault, searchapi/ISearchScopeRule::get_IsDefault
f1_keywords:
- searchapi/ISearchScopeRule.get_IsDefault
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Searchapi.h
api_name:
- ISearchScopeRule.get_IsDefault
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchScopeRule::get_IsDefault


## -description


Gets a value that identifies whether this is a default rule.


## -parameters




### -param pfIsDefault [out, retval]

Type: <b>BOOL*</b>

On return, points to the <b>TRUE</b> for default rules and <b>FALSE</b> otherwise.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



