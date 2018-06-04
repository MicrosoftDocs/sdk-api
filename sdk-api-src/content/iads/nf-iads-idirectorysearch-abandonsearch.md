---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDirectorySearch::AbandonSearch


## -description


The <b>IDirectorySearch::AbandonSearch</b> method abandons a search initiated by an earlier call to the  <a href="https://msdn.microsoft.com/7514b372-1a7a-4a42-a814-af70a727c477">ExecuteSearch</a> method.


## -parameters




### -param phSearchResult






#### - hSearchHandle [in]

Provides a handle to the search context.


## -returns



This method returns the standard return values, including S_OK if the first row is obtained successfully.

For other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



<b>IDirectorySearch::AbandonSearch</b> may be used if the Page_Size or Asynchronous options can be specified through  <a href="https://msdn.microsoft.com/1c5b3f72-6165-41ad-99d4-d68bc12ac10b">IDirectorySearch::SetSearchPreference</a> before the search is executed.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LPWSTR pszAttr[] = { L"ADsPath", L"Name", L"samAccountName" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount= sizeof(pszAttr)/sizeof(LPWSTR);
////////////////////////////////////////////////////////////////////
// NOTE: Assume that m_pSearch is an IDirectorySearch pointer to the 
// object at the base of the search, and that the appropriate search 
// preferences have been set.
// For brevity, omit error handling.
////////////////////////////////////////////////////////////////////
 
// Search for all users with a last name that starts with h.
hr = m_pSearch-&gt;ExecuteSearch(L"(&amp;(objectClass=user)(sn=h*))", pszAttr, dwCount, &amp;hSearch );
while( m_pSearch-&gt;GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
{
    // Get the samAccountName
    hr = m_pSearch-&gt;GetColumn( hSearch, pszAttr[2], &amp;col );
    if ( FAILED(hr) )
    {
        hr = m_pSearch-&gt;AbandonSearch( hSearch );
        hr = m_pSearch-&gt;CloseSearchHandle(hSearch);
        m_pSearch-&gt;Release();
        break;
    }
    if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
       printf("%S\n", col.pADsValues-&gt;CaseIgnoreString); 
   m_pSearch-&gt;FreeColumn( &amp;col );
}
 
m_pSearch-&gt;CloseSearchHandle( hSearch );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>



<a href="https://msdn.microsoft.com/7514b372-1a7a-4a42-a814-af70a727c477">IDirectorySearch::ExecuteSearch</a>



<a href="https://msdn.microsoft.com/1c5b3f72-6165-41ad-99d4-d68bc12ac10b">IDirectorySearch::SetSearchPreference</a>
 

 

