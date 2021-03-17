---
UID: NF:iads.IDirectorySearch.GetPreviousRow
title: IDirectorySearch::GetPreviousRow (iads.h)
description: The IDirectorySearch::GetPreviousRow method gets the previous row of the search result. If the provider does not provide cursor support, it should return E_NOTIMPL.
helpviewer_keywords: ["GetPreviousRow","GetPreviousRow method [ADSI]","GetPreviousRow method [ADSI]","IDirectorySearch interface","IDirectorySearch interface [ADSI]","GetPreviousRow method","IDirectorySearch.GetPreviousRow","IDirectorySearch::GetPreviousRow","_ds_idirectorysearch_getpreviousrow","adsi.idirectorysearch__getpreviousrow","adsi.idirectorysearch_getpreviousrow","iads/IDirectorySearch::GetPreviousRow"]
old-location: adsi\idirectorysearch_getpreviousrow.htm
tech.root: adsi
ms.assetid: fccc9763-c64d-474b-a0c0-9bc9d4e34d65
ms.date: 12/05/2018
ms.keywords: GetPreviousRow, GetPreviousRow method [ADSI], GetPreviousRow method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],GetPreviousRow method, IDirectorySearch.GetPreviousRow, IDirectorySearch::GetPreviousRow, _ds_idirectorysearch_getpreviousrow, adsi.idirectorysearch__getpreviousrow, adsi.idirectorysearch_getpreviousrow, iads/IDirectorySearch::GetPreviousRow
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
 - IDirectorySearch::GetPreviousRow
 - iads/IDirectorySearch::GetPreviousRow
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
 - IDirectorySearch.GetPreviousRow
---

# IDirectorySearch::GetPreviousRow


## -description

The <b>IDirectorySearch::GetPreviousRow</b> method gets the previous row of the search result. If the provider does not provide cursor support, it should return <b>E_NOTIMPL</b>.

## -parameters

### -param hSearchResult [in]

Provides a handle to the search context.

## -returns

This method returns the standard return values, as well as the following:

For other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

When the <b>ADS_SEARCHPREF_CACHE_RESULTS</b> flag is not set, only forward scrolling is permitted, because the client might not cache all the query results.


#### Examples


```cpp
hr = m_pSearch->ExecuteSearch(L"(&(objectCategory=user)(st=WA))", pszAttr, dwCount, &hSearch );
if ( SUCCEEDED(hr) )
{
   while(  m_pSearch->GetNextRow(hSearch)  != S_ADS_NOMORE_ROWS )
   {
      /* Get the data */
   }
   // Print it backward
   hr = m_pSearch->GetPreviousRow( hSearch );
   while( hr != S_ADS_NOMORE_ROWS  &&  hr != E_NOTIMPL)
   {
      /* Get the data */
   }
   m_pSearch->CloseSearchHandle(hSearch);
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>