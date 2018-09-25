---
UID: NF:iads.IDirectorySearch.GetFirstRow
title: IDirectorySearch::GetFirstRow
author: windows-sdk-content
description: The GetFirstRow method gets the first row of a search result. This method will issue or reissue a new search, even if this method has been called before.
old-location: adsi\idirectorysearch_getfirstrow.htm
tech.root: ADSI
ms.assetid: 99ece6d1-3963-40bc-993e-f03aa9039c2d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetFirstRow, GetFirstRow method [ADSI], GetFirstRow method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],GetFirstRow method, IDirectorySearch.GetFirstRow, IDirectorySearch::GetFirstRow, _ds_idirectorysearch_getfirstrow, adsi.idirectorysearch__getfirstrow, adsi.idirectorysearch_getfirstrow, iads/IDirectorySearch::GetFirstRow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectorySearch::GetFirstRow


## -description


The <b>GetFirstRow</b> method gets the first row of a search result. This method will issue or reissue a new search, even if this method has been called before.


## -parameters




### -param hSearchResult

TBD




#### - hSearchHandle [in]

Contains the search handle obtained by calling <a href="https://msdn.microsoft.com/7514b372-1a7a-4a42-a814-af70a727c477">IDirectorySearch::ExecuteSearch</a>.


## -returns



This method returns the standard return values, as well as the following:
      

For more information,  see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



When the <b>ADS_SEARCHPREF_CACHE_RESULTS</b> flag is not set, that is, <b>FALSE</b>, only forward scrolling is permitted, because the client might not cache all the query results. Calling <b>GetFirstRow</b> more than once from the same row requires some back-scrolling and could result in erroneous outcomes for a paged or an asynchronous search initiated through OLE DB when the results are not guaranteed to remain in the cache.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>hr = m_pSearch-&gt;ExecuteSearch(L"(objectCategory=contact)", pszAttr, dwCount, &amp;hSearch);
if(SUCCEEDED(hr))
{
    while(SUCCEEDED(hr = m_pSearch-&gt;GetNextRow(hSearch)))
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

            ADsGetLastError(&amp;dwError, szError, 512, szProvider, 512);
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
    
    m_pSearch-&gt;CloseSearchHandle(hSearch);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>



<a href="https://msdn.microsoft.com/7514b372-1a7a-4a42-a814-af70a727c477">IDirectorySearch::ExecuteSearch</a>
 

 

