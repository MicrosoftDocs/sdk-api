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

# TTEnableEmbeddingForFacename function


## -description


Adds or removes facenames from the typeface exclusion list.


## -parameters




### -param lpszFacename [in]

Pointer to the facename of the font to be added or removed from the typeface exclusion list.


### -param bEnable [in]

Boolean controlling operation on typeface exclusion list. If nonzero, then the facename will be removed from the list; if zero, the facename will be added to the list.


## -returns



If successful, returns E_NONE.

The facename indicated by <i>lpszFacename</i> will be added or removed from the typeface exclusion list.

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding-Function Error Messages</a>.




## -remarks



The function <b>TTEnableEmbeddingForFacename</b> uses a typeface exclusion list to control whether a specific font can be embedded. This list identifies all fonts that should NOT be embedded and is shared by all authoring clients on a single system.

An authoring client can embed fonts without referencing the typeface exclusion list (that is, without using <b>TTEnableEmbeddingForFacename</b>). Embedding fonts in a document results in the following tradeoffs.

<ul>
<li>Provides all font information within a document so the appropriate client can render the document.</li>
<li>Adds size to a document.</li>
<li>Complicates streaming read and write operations to a document and uses more processing bandwidth.</li>
<li>Makes a document less readable by other applications.</li>
<li>Can leave copyright issues unmanaged, if the type exclusion list is not used.</li>
</ul>
Two additional functions, <a href="https://msdn.microsoft.com/f1e3112b-d840-45eb-bb99-416319ed9e15">TTIsEmbeddingEnabled</a> and <a href="https://msdn.microsoft.com/1f494bb1-62c4-45c4-b1a5-df6842d94dcc">TTIsEmbeddingEnabledForFacename</a>, access the typeface exclusion list to provide enabling status.

The typeface exclusion list is stored in the registry key <b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Shared Tools\t2embed</b>. The default typeface exclusion list should contain the following named value entries representing the Microsoft Windows core fonts.

<table>
<tr>
<th>Value name</th>
<th>Data type</th>
<th>Data value</th>
</tr>
<tr>
<td>Arial</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Arial Bold</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Arial Bold Italic</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Arial Italic</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Courier New</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Courier New Bold</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Courier New Bold Italic</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Courier New Italic</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Times New Roman</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Times New Roman Bold</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Times New Roman Bold Italic</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
<tr>
<td>Times New Roman Italic</td>
<td>REG_DWORD</td>
<td>0</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f1e3112b-d840-45eb-bb99-416319ed9e15">TTIsEmbeddingEnabled</a>



<a href="https://msdn.microsoft.com/1f494bb1-62c4-45c4-b1a5-df6842d94dcc">TTIsEmbeddingEnabledForFacename</a>
 

 

