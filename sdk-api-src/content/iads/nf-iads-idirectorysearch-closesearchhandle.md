---
UID: NF:iads.IDirectorySearch.CloseSearchHandle
title: IDirectorySearch::CloseSearchHandle (iads.h)
description: The IDirectorySearch::CloseSearchHandle method closes the handle to a search result and frees the associated memory.
helpviewer_keywords: ["CloseSearchHandle","CloseSearchHandle method [ADSI]","CloseSearchHandle method [ADSI]","IDirectorySearch interface","IDirectorySearch interface [ADSI]","CloseSearchHandle method","IDirectorySearch.CloseSearchHandle","IDirectorySearch::CloseSearchHandle","_ds_idirectorysearch_closesearchhandle","adsi.idirectorysearch__closesearchhandle","adsi.idirectorysearch_closesearchhandle","iads/IDirectorySearch::CloseSearchHandle"]
old-location: adsi\idirectorysearch_closesearchhandle.htm
tech.root: adsi
ms.assetid: a233c67b-4747-4417-bec8-86b27147863c
ms.date: 12/05/2018
ms.keywords: CloseSearchHandle, CloseSearchHandle method [ADSI], CloseSearchHandle method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],CloseSearchHandle method, IDirectorySearch.CloseSearchHandle, IDirectorySearch::CloseSearchHandle, _ds_idirectorysearch_closesearchhandle, adsi.idirectorysearch__closesearchhandle, adsi.idirectorysearch_closesearchhandle, iads/IDirectorySearch::CloseSearchHandle
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll; Adsldp.dll; Adsldpc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectorySearch::CloseSearchHandle
 - iads/IDirectorySearch::CloseSearchHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
 - Adsldp.dll
 - Adsldpc.dll
api_name:
 - IDirectorySearch.CloseSearchHandle
---

# IDirectorySearch::CloseSearchHandle


## -description

The <b>IDirectorySearch::CloseSearchHandle</b> method closes the handle to a search result and frees the associated memory.

## -parameters

### -param hSearchResult [in]

Provides a handle to the search result to be closed.

## -returns

This method returns the standard return values, as well as the following:

For other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The process that implements the <b>IDirectorySearch::CloseSearchHandle</b> method must also be responsible for freeing all memory allocated by the  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">IDirectorySearch::ExecuteSearch</a> method, including the search result and the search result handle.

The caller may call this method only once for each opened search handle and must use the <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">IDirectorySearch::ExecuteSearch</a> method to obtain a new search handle after issuing <b>IDirectorySearch::CloseSearchHandle</b>.


#### Examples


```cpp
ADS_SEARCH_HANDLE hSearch;
HRESULT hr;
hr = m_pSearch->ExecuteSearch(L"(&(objectCategory=user)(l=Redmond))", pszAttr, dwCount, &hSearch );
if ( SUCCEEDED(hr) )
{
   // Omit getting the data
   m_pSearch->CloseSearchHandle(hSearch);
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">IDirectorySearch::ExecuteSearch</a>