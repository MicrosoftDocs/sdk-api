---
UID: NF:searchapi.ISearchCatalogManager2.PrioritizeMatchingURLs
title: ISearchCatalogManager2::PrioritizeMatchingURLs (searchapi.h)
description: Instructs the indexer to give a higher priority to indexing items that have URLs that match a specified pattern. These items will then have a higher priority than other indexing tasks.
helpviewer_keywords: ["ISearchCatalogManager2 interface [search]","PrioritizeMatchingURLs method","ISearchCatalogManager2.PrioritizeMatchingURLs","ISearchCatalogManager2::PrioritizeMatchingURLs","PrioritizeMatchingURLs","PrioritizeMatchingURLs method [search]","PrioritizeMatchingURLs method [search]","ISearchCatalogManager2 interface","_search_ISearchCatalogManager2_PrioritizeMatchingURLs","search._search_ISearchCatalogManager2_PrioritizeMatchingURLs","searchapi/ISearchCatalogManager2::PrioritizeMatchingURLs"]
old-location: search\_search_ISearchCatalogManager2_PrioritizeMatchingURLs.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager2\prioritizematchingurls.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager2 interface [search],PrioritizeMatchingURLs method, ISearchCatalogManager2.PrioritizeMatchingURLs, ISearchCatalogManager2::PrioritizeMatchingURLs, PrioritizeMatchingURLs, PrioritizeMatchingURLs method [search], PrioritizeMatchingURLs method [search],ISearchCatalogManager2 interface, _search_ISearchCatalogManager2_PrioritizeMatchingURLs, search._search_ISearchCatalogManager2_PrioritizeMatchingURLs, searchapi/ISearchCatalogManager2::PrioritizeMatchingURLs
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcatalog.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Search (WS) 4.0
ms.custom: 19H1
f1_keywords:
 - ISearchCatalogManager2::PrioritizeMatchingURLs
 - searchapi/ISearchCatalogManager2::PrioritizeMatchingURLs
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
 - ISearchCatalogManager2.PrioritizeMatchingURLs
---

# ISearchCatalogManager2::PrioritizeMatchingURLs


## -description

Instructs the indexer to give a higher priority to indexing items that have URLs that match a specified pattern. These items will then have a higher priority than other indexing tasks.

## -parameters

### -param pszPattern [in]

Type: <b>LPCWSTR</b>

A string specifying the URL pattern that defines items that failed indexing and need re-indexing.

### -param dwPrioritizeFlags [in]

Type: <b><a href="/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a></b>

A value from the <a href="/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a> enumeration that specifies how to process items that the indexer has failed to index.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.

## -remarks

The <i>pszPattern</i> string must specify a pattern than matches the entire item URL. You can use the asterisk wildcard character to create your pattern string.
            

The <i>PRIORITIZE_FLAG_IGNOREFAILURECOUNT</i> flag is valid only in combination with the <i>PRIORITIZE_FLAG_RETRYFAILEDITEMS</i> flag.
            


#### Examples

The following examples show the use of the asterisk wildcard character and of the <i>PRIORITIZE_FLAG_IGNOREFAILURECOUNT</i>.


```cpp
hr = cpSearchCatalogManager2->PrioritizeMatchingURLs("mapi://{<SID>}/Mailbox - Boyer Zara/*",
            PRIORITIZE_FLAG_RETRYFAILEDITEMS);
```



```cpp
hr = cpSearchCatalogManager2->PrioritizeMatchingURLs("file:f:/Project Files/*",
            PRIORITIZE_FLAG_RETRYFAILEDITEMS);
```



```cpp
hr = cpSearchCatalogManager2->PrioritizeMatchingURLs("file:f:/Project Files/*.docx",
            PRIORITIZE_FLAG_RETRYFAILEDITEMS | PRIORITIZE_FLAG_IGNOREFAILURECOUNT);
```

