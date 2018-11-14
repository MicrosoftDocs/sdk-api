---
UID: NF:iads.IDirectorySearch.GetPreviousRow
title: IDirectorySearch::GetPreviousRow
author: windows-sdk-content
description: The IDirectorySearch::GetPreviousRow method gets the previous row of the search result. If the provider does not provide cursor support, it should return E_NOTIMPL.
old-location: adsi\idirectorysearch_getpreviousrow.htm
tech.root: ADSI
ms.assetid: fccc9763-c64d-474b-a0c0-9bc9d4e34d65
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPreviousRow, GetPreviousRow method [ADSI], GetPreviousRow method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],GetPreviousRow method, IDirectorySearch.GetPreviousRow, IDirectorySearch::GetPreviousRow, _ds_idirectorysearch_getpreviousrow, adsi.idirectorysearch__getpreviousrow, adsi.idirectorysearch_getpreviousrow, iads/IDirectorySearch::GetPreviousRow
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
 - IDirectorySearch.GetPreviousRow
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
- IDirectorySearch.GetPreviousRow
: 
---

# IDirectorySearch::GetPreviousRow


## -description


The <b>IDirectorySearch::GetPreviousRow</b> method gets the previous row of the search result. If the provider does not provide cursor support, it should return <b>E_NOTIMPL</b>.


## -parameters




### -param hSearchResult

TBD




#### - hSearchHandle [in]

Provides a handle to the search context.


## -returns



This method returns the standard return values, as well as the following:

For other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



When the <b>ADS_SEARCHPREF_CACHE_RESULTS</b> flag is not set, only forward scrolling is permitted, because the client might not cache all the query results.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>hr = m_pSearch-&gt;ExecuteSearch(L"(&amp;(objectCategory=user)(st=WA))", pszAttr, dwCount, &amp;hSearch );
if ( SUCCEEDED(hr) )
{
   while(  m_pSearch-&gt;GetNextRow(hSearch)  != S_ADS_NOMORE_ROWS )
   {
      /* Get the data */
   }
   // Print it backward
   hr = m_pSearch-&gt;GetPreviousRow( hSearch );
   while( hr != S_ADS_NOMORE_ROWS  &amp;&amp;  hr != E_NOTIMPL)
   {
      /* Get the data */
   }
   m_pSearch-&gt;CloseSearchHandle(hSearch);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>
 

 

