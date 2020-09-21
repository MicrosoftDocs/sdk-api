---
UID: NF:iads.IDirectorySearch.GetNextRow
title: IDirectorySearch::GetNextRow (iads.h)
description: Gets the next row of the search result.
helpviewer_keywords: ["GetNextRow","GetNextRow method [ADSI]","GetNextRow method [ADSI]","IDirectorySearch interface","IDirectorySearch interface [ADSI]","GetNextRow method","IDirectorySearch.GetNextRow","IDirectorySearch::GetNextRow","_ds_idirectorysearch_getnextrow","adsi.idirectorysearch__getnextrow","adsi.idirectorysearch_getnextrow","iads/IDirectorySearch::GetNextRow"]
old-location: adsi\idirectorysearch_getnextrow.htm
tech.root: adsi
ms.assetid: 9fb0b765-0162-418d-b0cd-7e9b1b53e1b9
ms.date: 12/05/2018
ms.keywords: GetNextRow, GetNextRow method [ADSI], GetNextRow method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],GetNextRow method, IDirectorySearch.GetNextRow, IDirectorySearch::GetNextRow, _ds_idirectorysearch_getnextrow, adsi.idirectorysearch__getnextrow, adsi.idirectorysearch_getnextrow, iads/IDirectorySearch::GetNextRow
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
 - IDirectorySearch::GetNextRow
 - iads/IDirectorySearch::GetNextRow
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
 - IDirectorySearch.GetNextRow
---

# IDirectorySearch::GetNextRow


## -description

The <b>GetNextRow</b> method gets the next row of the search result. If  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow">IDirectorySearch::GetFirstRow</a> has not been called, <b>GetNextRow</b> will issue a new search beginning from the first row. Otherwise, this method will advance to the next row.

## -parameters

### -param hSearchResult [in]

Contains the search handle obtained by calling <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">IDirectorySearch::ExecuteSearch</a>.

## -returns

This method returns the standard return values, as well as the following:

For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

When the <b>ADS_SEARCHPREF_CACHE_RESULTS</b> flag is not set, only forward scrolling is permitted, because the client might not cache all the query results.

The directory provider may limit the maximum number of rows available in a search. For example, on a Windows domain, the maximum number of rows that will be provided in an Active Directory search is 1000 rows. If the search results in more than the row limit, a paged search must be performed to obtain all rows in the search. For more information about paged searches, see <a href="/windows/desktop/ADSI/paging-with-idirectorysearch">Paging with IDirectorySearch</a>.


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



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetlasterror">ADsGetLastError</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">IDirectorySearch::ExecuteSearch</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow">IDirectorySearch::GetFirstRow</a>