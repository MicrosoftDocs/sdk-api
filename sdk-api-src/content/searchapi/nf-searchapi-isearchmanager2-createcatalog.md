---
UID: NF:searchapi.ISearchManager2.CreateCatalog
title: ISearchManager2::CreateCatalog (searchapi.h)
description: Creates a new custom catalog in the Windows Search indexer and returns a reference to it.
helpviewer_keywords: ["CreateCatalog","CreateCatalog method [search]","CreateCatalog method [search]","ISearchManager2 interface","ISearchManager2 interface [search]","CreateCatalog method","ISearchManager2.CreateCatalog","ISearchManager2::CreateCatalog","search.isearchmanager2_createcatalog","searchapi/ISearchManager2::CreateCatalog"]
old-location: search\isearchmanager2_createcatalog.htm
tech.root: search
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
ms.date: 12/05/2018
ms.keywords: CreateCatalog, CreateCatalog method [search], CreateCatalog method [search],ISearchManager2 interface, ISearchManager2 interface [search],CreateCatalog method, ISearchManager2.CreateCatalog, ISearchManager2::CreateCatalog, search.isearchmanager2_createcatalog, searchapi/ISearchManager2::CreateCatalog
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchManager2::CreateCatalog
 - searchapi/ISearchManager2::CreateCatalog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - searchapi.h
api_name:
 - ISearchManager2.CreateCatalog
---

# ISearchManager2::CreateCatalog


## -description

Creates a new custom catalog in the Windows Search indexer and returns a reference to it.

## -parameters

### -param pszCatalog [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Name of catalog to create. Can be any name selected by the caller, must contain only standard alphanumeric characters and underscore.

### -param ppCatalogManager [out]

Type: <b><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a>**</b>

On success a reference to the created catalog is returned as an <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a> interface pointer. The Release() must be called on this interface after the calling application has finished using it.

## -returns

Type: <b>HRESULT</b>

HRESULT indicating status of operation:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Catalog did not previously exist and was created. Reference to catalog returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Catalog previously existed, reference to catalog returned.

</td>
</tr>
</table>
 

FAILED HRESULT: Failure creating catalog or invalid arguments passed.

## -remarks

Called to create a new catalog in the Windows Search indexer.
After creation, the methods on the returned  <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalog</a> manager can be used to add locations to be indexed, monitor indexing process, and construct queries to send to the indexer and get results. For more information, see [Managing the Index](/windows/win32/search/-search-3x-wds-mngidx-overview).

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2">ISearchManager2</a>
