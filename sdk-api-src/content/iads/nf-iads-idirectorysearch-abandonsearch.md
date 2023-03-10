---
UID: NF:iads.IDirectorySearch.AbandonSearch
title: IDirectorySearch::AbandonSearch (iads.h)
description: The IDirectorySearch::AbandonSearch method abandons a search initiated by an earlier call to the ExecuteSearch method.
helpviewer_keywords: ["AbandonSearch","AbandonSearch method [ADSI]","AbandonSearch method [ADSI]","IDirectorySearch interface","IDirectorySearch interface [ADSI]","AbandonSearch method","IDirectorySearch.AbandonSearch","IDirectorySearch::AbandonSearch","_ds_idirectorysearch_abandonsearch","adsi.idirectorysearch__abandonsearch","adsi.idirectorysearch_abandonsearch","iads/IDirectorySearch::AbandonSearch"]
old-location: adsi\idirectorysearch_abandonsearch.htm
tech.root: adsi
ms.assetid: cf220625-0aac-42ce-a15f-c44766693cf8
ms.date: 12/05/2018
ms.keywords: AbandonSearch, AbandonSearch method [ADSI], AbandonSearch method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],AbandonSearch method, IDirectorySearch.AbandonSearch, IDirectorySearch::AbandonSearch, _ds_idirectorysearch_abandonsearch, adsi.idirectorysearch__abandonsearch, adsi.idirectorysearch_abandonsearch, iads/IDirectorySearch::AbandonSearch
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
 - IDirectorySearch::AbandonSearch
 - iads/IDirectorySearch::AbandonSearch
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
 - IDirectorySearch.AbandonSearch
---

# IDirectorySearch::AbandonSearch


## -description

The <b>IDirectorySearch::AbandonSearch</b> method abandons a search initiated by an earlier call to the  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">ExecuteSearch</a> method.

## -parameters

### -param phSearchResult [in]

Provides a handle to the search context.

## -returns

This method returns the standard return values, including S_OK if the first row is obtained successfully.

For other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

<b>IDirectorySearch::AbandonSearch</b> may be used if the Page_Size or Asynchronous options can be specified through  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a> before the search is executed.


#### Examples


```cpp
LPWSTR pszAttr[] = { L"ADsPath", L"Name", L"samAccountName" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount= sizeof(pszAttr)/sizeof(LPWSTR);
////////////////////////////////////////////////////////////////////
// NOTE: Assume that m_pSearch is an IDirectorySearch pointer to the 
// object at the base of the search, and that the appropriate search 
// preferences have been set.
// For brevity, omit error handling.
////////////////////////////////////////////////////////////////////
 
// Search for all users with a last name that starts with h.
hr = m_pSearch->ExecuteSearch(L"(&(objectClass=user)(sn=h*))", pszAttr, dwCount, &hSearch );
while( m_pSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
{
    // Get the samAccountName
    hr = m_pSearch->GetColumn( hSearch, pszAttr[2], &col );
    if ( FAILED(hr) )
    {
        hr = m_pSearch->AbandonSearch( hSearch );
        hr = m_pSearch->CloseSearchHandle(hSearch);
        m_pSearch->Release();
        break;
    }
    if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
       printf("%S\n", col.pADsValues->CaseIgnoreString); 
   m_pSearch->FreeColumn( &col );
}
 
m_pSearch->CloseSearchHandle( hSearch );
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">IDirectorySearch::ExecuteSearch</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a>