---
UID: NF:iads.IDirectorySearch.GetFirstRow
title: IDirectorySearch::GetFirstRow (iads.h)
description: The GetFirstRow method gets the first row of a search result. This method will issue or reissue a new search, even if this method has been called before.
helpviewer_keywords: ["GetFirstRow","GetFirstRow method [ADSI]","GetFirstRow method [ADSI]","IDirectorySearch interface","IDirectorySearch interface [ADSI]","GetFirstRow method","IDirectorySearch.GetFirstRow","IDirectorySearch::GetFirstRow","_ds_idirectorysearch_getfirstrow","adsi.idirectorysearch__getfirstrow","adsi.idirectorysearch_getfirstrow","iads/IDirectorySearch::GetFirstRow"]
old-location: adsi\idirectorysearch_getfirstrow.htm
tech.root: adsi
ms.assetid: 99ece6d1-3963-40bc-993e-f03aa9039c2d
ms.date: 12/05/2018
ms.keywords: GetFirstRow, GetFirstRow method [ADSI], GetFirstRow method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],GetFirstRow method, IDirectorySearch.GetFirstRow, IDirectorySearch::GetFirstRow, _ds_idirectorysearch_getfirstrow, adsi.idirectorysearch__getfirstrow, adsi.idirectorysearch_getfirstrow, iads/IDirectorySearch::GetFirstRow
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
 - IDirectorySearch::GetFirstRow
 - iads/IDirectorySearch::GetFirstRow
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
 - IDirectorySearch.GetFirstRow
---

# IDirectorySearch::GetFirstRow


## -description

The <b>GetFirstRow</b> method gets the first row of a search result. This method will issue or reissue a new search, even if this method has been called before.

## -parameters

### -param hSearchResult [in]

Contains the search handle obtained by calling <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">IDirectorySearch::ExecuteSearch</a>.

## -returns

This method returns the standard return values, as well as the following:
      

For more information,  see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

When the <b>ADS_SEARCHPREF_CACHE_RESULTS</b> flag is not set, that is, <b>FALSE</b>, only forward scrolling is permitted, because the client might not cache all the query results. Calling <b>GetFirstRow</b> more than once from the same row requires some back-scrolling and could result in erroneous outcomes for a paged or an asynchronous search initiated through OLE DB when the results are not guaranteed to remain in the cache.


#### Examples


```cpp
hr = m_pSearch->ExecuteSearch(L"(objectCategory=contact)", pszAttr, dwCount, &hSearch);
if(SUCCEEDED(hr))
{
    while(SUCCEEDED(hr = m_pSearch->GetNextRow(hSearch)))
    {
        if(S_OK == hr)
        {
            // Get the data.
        }
        else if(S_ADS_NOMORE_ROWS == hr)
        {
            // Call ADsGetLastError to see if the search is waiting for a response.
            DWORD dwError = ERROR_SUCCESS;
            WCHAR szError[512];
            WCHAR szProvider[512];

            ADsGetLastError(&dwError, szError, 512, szProvider, 512);
            if(ERROR_MORE_DATA != dwError)
            {
                break;
            }
        }
        else
        {
            break;
        }
    }
    
    m_pSearch->CloseSearchHandle(hSearch);
}

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">IDirectorySearch::ExecuteSearch</a>