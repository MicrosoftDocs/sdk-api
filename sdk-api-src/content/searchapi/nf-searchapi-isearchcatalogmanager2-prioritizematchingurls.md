---
UID: NF:searchapi.ISearchCatalogManager2.PrioritizeMatchingURLs
title: ISearchCatalogManager2::PrioritizeMatchingURLs
author: windows-sdk-content
description: Instructs the indexer to give a higher priority to indexing items that have URLs that match a specified pattern. These items will then have a higher priority than other indexing tasks.
old-location: search\_search_ISearchCatalogManager2_PrioritizeMatchingURLs.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager2\prioritizematchingurls.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchCatalogManager2 interface [search],PrioritizeMatchingURLs method, ISearchCatalogManager2.PrioritizeMatchingURLs, ISearchCatalogManager2::PrioritizeMatchingURLs, PrioritizeMatchingURLs, PrioritizeMatchingURLs method [search], PrioritizeMatchingURLs method [search],ISearchCatalogManager2 interface, _search_ISearchCatalogManager2_PrioritizeMatchingURLs, search._search_ISearchCatalogManager2_PrioritizeMatchingURLs, searchapi/ISearchCatalogManager2::PrioritizeMatchingURLs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcatalog.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchCatalogManager2.PrioritizeMatchingURLs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchCatalogManager2::PrioritizeMatchingURLs


## -description


Instructs the indexer to give a higher priority to indexing items that have URLs that match a specified pattern. These items will then have a higher priority than other indexing tasks.


## -parameters




### -param pszPattern [in]

Type: <b>LPCWSTR</b>

A string specifying the URL pattern that defines items that failed indexing and need re-indexing.


### -param dwPrioritizeFlags [in]

Type: <b><a href="https://msdn.microsoft.com/554d405e-c117-4597-9612-20cd6088ebef">PRIORITIZE_FLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/554d405e-c117-4597-9612-20cd6088ebef">PRIORITIZE_FLAGS</a> enumeration that specifies how to process items that the indexer has failed to index.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.




## -remarks



The <i>pszPattern</i> string must specify a pattern than matches the entire item URL. You can use the asterisk wildcard character to create your pattern string.
            


            The <i>PRIORITIZE_FLAG_IGNOREFAILURECOUNT</i> flag is valid only in combination with the <i>PRIORITIZE_FLAG_RETRYFAILEDITEMS</i> flag.
            


#### Examples

The following examples show the use of the asterisk wildcard character and of the <i>PRIORITIZE_FLAG_IGNOREFAILURECOUNT</i>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>hr = cpSearchCatalogManager2-&gt;PrioritizeMatchingURLs("mapi://{&lt;SID&gt;}/Mailbox - Boyer Zara/*",
            PRIORITIZE_FLAG_RETRYFAILEDITEMS);</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>hr = cpSearchCatalogManager2-&gt;PrioritizeMatchingURLs("file:f:/Project Files/*",
            PRIORITIZE_FLAG_RETRYFAILEDITEMS);</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>hr = cpSearchCatalogManager2-&gt;PrioritizeMatchingURLs("file:f:/Project Files/*.docx",
            PRIORITIZE_FLAG_RETRYFAILEDITEMS | PRIORITIZE_FLAG_IGNOREFAILURECOUNT);</pre>
</td>
</tr>
</table></span></div>


