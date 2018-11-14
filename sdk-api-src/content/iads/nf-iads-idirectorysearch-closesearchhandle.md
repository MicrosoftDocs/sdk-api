---
UID: NF:iads.IDirectorySearch.CloseSearchHandle
title: IDirectorySearch::CloseSearchHandle
author: windows-sdk-content
description: The IDirectorySearch::CloseSearchHandle method closes the handle to a search result and frees the associated memory.
old-location: adsi\idirectorysearch_closesearchhandle.htm
tech.root: ADSI
ms.assetid: a233c67b-4747-4417-bec8-86b27147863c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CloseSearchHandle, CloseSearchHandle method [ADSI], CloseSearchHandle method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],CloseSearchHandle method, IDirectorySearch.CloseSearchHandle, IDirectorySearch::CloseSearchHandle, _ds_idirectorysearch_closesearchhandle, adsi.idirectorysearch__closesearchhandle, adsi.idirectorysearch_closesearchhandle, iads/IDirectorySearch::CloseSearchHandle
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
 - IDirectorySearch.CloseSearchHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- iads.h
: 
- IDirectorySearch.CloseSearchHandle
: 
---

# IDirectorySearch::CloseSearchHandle


## -description


The <b>IDirectorySearch::CloseSearchHandle</b> method closes the handle to a search result and frees the associated memory.


## -parameters




### -param hSearchResult

TBD




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
 

 

