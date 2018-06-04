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


