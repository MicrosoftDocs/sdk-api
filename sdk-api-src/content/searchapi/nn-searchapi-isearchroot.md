---
UID: NN:searchapi.ISearchRoot
title: ISearchRoot (searchapi.h)
description: Provides methods for manipulating a search root. Changes to property members are applied to any URL that falls under the search root. A URL falls under a search root if it matches the search root URL or is a hierarchical child of that URL.
helpviewer_keywords: ["ISearchRoot","ISearchRoot interface [search]","ISearchRoot interface [search]","described","_search_ISearchRoot","search._search_ISearchRoot","searchapi/ISearchRoot"]
old-location: search\_search_ISearchRoot.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\isearchroot.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot, ISearchRoot interface [search], ISearchRoot interface [search],described, _search_ISearchRoot, search._search_ISearchRoot, searchapi/ISearchRoot
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ISearchRoot
 - searchapi/ISearchRoot
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
 - ISearchRoot
---

# ISearchRoot interface


## -description

Provides methods for manipulating a search root. Changes to property members are applied to any URL that falls under the search root. A URL falls under a search root if it matches the search root URL or is a hierarchical child of that URL.

## -inheritance

The <b>ISearchRoot</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchRoot</b> also has these types of members:

## -remarks

For a sample that demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations, see the [CrawlScopeCommandLine](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine) sample.

## -see-also

<a href="/windows/desktop/search/-search-3x-wds-extidx-csm">Using the Crawl Scope Manager</a>
