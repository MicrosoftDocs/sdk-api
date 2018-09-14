---
UID: NF:iads.IDirectorySearch.AbandonSearch
title: IDirectorySearch::AbandonSearch
author: windows-sdk-content
description: The IDirectorySearch::AbandonSearch method abandons a search initiated by an earlier call to the ExecuteSearch method.
old-location: adsi\idirectorysearch_abandonsearch.htm
tech.root: ADSI
ms.assetid: cf220625-0aac-42ce-a15f-c44766693cf8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AbandonSearch, AbandonSearch method [ADSI], AbandonSearch method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],AbandonSearch method, IDirectorySearch.AbandonSearch, IDirectorySearch::AbandonSearch, _ds_idirectorysearch_abandonsearch, adsi.idirectorysearch__abandonsearch, adsi.idirectorysearch_abandonsearch, iads/IDirectorySearch::AbandonSearch
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
 - IDirectorySearch.AbandonSearch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectorySearch::AbandonSearch


## -description


The <b>IDirectorySearch::AbandonSearch</b> method abandons a search initiated by an earlier call to the  <a href="https://msdn.microsoft.com/7514b372-1a7a-4a42-a814-af70a727c477">ExecuteSearch</a> method.


## -parameters




### -param phSearchResult

TBD




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
 

 

