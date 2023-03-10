---
UID: NF:searchapi.ISearchScopeRule.get_PatternOrURL
title: ISearchScopeRule::get_PatternOrURL (searchapi.h)
description: Gets the pattern or URL for the rule. The scope rules determine what URLs or paths to include or exclude.
helpviewer_keywords: ["ISearchScopeRule interface [search]","get_PatternOrURL method","ISearchScopeRule.get_PatternOrURL","ISearchScopeRule::get_PatternOrURL","_search_ISearchScopeRule_get_PatternOrURL","get_PatternOrURL","get_PatternOrURL method [search]","get_PatternOrURL method [search]","ISearchScopeRule interface","search._search_ISearchScopeRule_get_PatternOrURL","searchapi/ISearchScopeRule::get_PatternOrURL"]
old-location: search\_search_ISearchScopeRule_get_PatternOrURL.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchscoperule\get_patternorurl.htm
ms.date: 12/05/2018
ms.keywords: ISearchScopeRule interface [search],get_PatternOrURL method, ISearchScopeRule.get_PatternOrURL, ISearchScopeRule::get_PatternOrURL, _search_ISearchScopeRule_get_PatternOrURL, get_PatternOrURL, get_PatternOrURL method [search], get_PatternOrURL method [search],ISearchScopeRule interface, search._search_ISearchScopeRule_get_PatternOrURL, searchapi/ISearchScopeRule::get_PatternOrURL
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
 - ISearchScopeRule::get_PatternOrURL
 - searchapi/ISearchScopeRule::get_PatternOrURL
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
 - ISearchScopeRule.get_PatternOrURL
---

# ISearchScopeRule::get_PatternOrURL


## -description

Gets the pattern or URL for the rule. The scope rules determine what URLs or paths to include or exclude.

## -parameters

### -param ppszPatternOrURL [out, retval]

Type: <b>LPWSTR*</b>

On return, contains the address of a pointer to a null-terminated, Unicode buffer that contains the pattern or URL string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A standard URL might look like this: <code> outlookexpress://{User sid}/{Identity}/Inbox)</code>

A pattern might look like this: <code> file:///c:\documents and settings\*\application data\* </code>

Only exclusion rules use patterns.

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.