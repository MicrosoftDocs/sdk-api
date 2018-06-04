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

# IDirectorySearch::CloseSearchHandle


## -description


The <b>IDirectorySearch::CloseSearchHandle</b> method closes the handle to a search result and frees the associated memory.


## -parameters




### -param hSearchResult






#### - hSearchHandle [in]

Provides a handle to the search result to be closed.


## -returns



This method returns the standard return values, as well as the following:

For other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The process that implements the <b>IDirectorySearch::CloseSearchHandle</b> method must also be responsible for freeing all memory allocated by the  <a href="https://msdn.microsoft.com/7514b372-1a7a-4a42-a814-af70a727c477">IDirectorySearch::ExecuteSearch</a> method, including the search result and the search result handle.

The caller may call this method only once for each opened search handle and must use the <a href="https://msdn.microsoft.com/7514b372-1a7a-4a42-a814-af70a727c477">IDirectorySearch::ExecuteSearch</a> method to obtain a new search handle after issuing <b>IDirectorySearch::CloseSearchHandle</b>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ADS_SEARCH_HANDLE hSearch;
HRESULT hr;
hr = m_pSearch-&gt;ExecuteSearch(L"(&amp;(objectCategory=user)(l=Redmond))", pszAttr, dwCount, &amp;hSearch );
if ( SUCCEEDED(hr) )
{
   // Omit getting the data
   m_pSearch-&gt;CloseSearchHandle(hSearch);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>



<a href="https://msdn.microsoft.com/7514b372-1a7a-4a42-a814-af70a727c477">IDirectorySearch::ExecuteSearch</a>
 

 

