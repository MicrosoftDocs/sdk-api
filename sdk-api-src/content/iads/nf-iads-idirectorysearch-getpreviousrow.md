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

# IDirectorySearch::GetPreviousRow


## -description


The <b>IDirectorySearch::GetPreviousRow</b> method gets the previous row of the search result. If the provider does not provide cursor support, it should return <b>E_NOTIMPL</b>.


## -parameters




### -param hSearchResult






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
 

 

