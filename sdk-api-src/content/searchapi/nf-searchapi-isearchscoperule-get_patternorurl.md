---
UID: NF:searchapi.ISearchScopeRule.get_PatternOrURL
title: ISearchScopeRule::get_PatternOrURL
author: windows-sdk-content
description: Gets the pattern or URL for the rule. The scope rules determine what URLs or paths to include or exclude.
old-location: search\_search_ISearchScopeRule_get_PatternOrURL.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchscoperule\get_patternorurl.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchScopeRule interface [search],get_PatternOrURL method, ISearchScopeRule.get_PatternOrURL, ISearchScopeRule::get_PatternOrURL, _search_ISearchScopeRule_get_PatternOrURL, get_PatternOrURL, get_PatternOrURL method [search], get_PatternOrURL method [search],ISearchScopeRule interface, search._search_ISearchScopeRule_get_PatternOrURL, searchapi/ISearchScopeRule::get_PatternOrURL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchScopeRule.get_PatternOrURL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A standard URL might look like this: <code> outlookexpress://{User sid}/{Identity}/Inbox)</code>

A pattern might look like this: <code> file:///c:\documents and settings\*\application data\* </code>

Only exclusion rules use patterns.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



