---
UID: NF:t2embapi.TTEnableEmbeddingForFacename
title: TTEnableEmbeddingForFacename function
author: windows-sdk-content
description: Adds or removes facenames from the typeface exclusion list.
old-location: gdi\ttenableembeddingforfacename.htm
tech.root: gdi
ms.assetid: 05d74bfb-28c4-4e1a-9e18-df868f8fa784
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TTEnableEmbeddingForFacename, TTEnableEmbeddingForFacename function [Windows GDI], _win32_TTEnableEmbeddingForFacename, gdi.ttenableembeddingforfacename, t2embapi/TTEnableEmbeddingForFacename
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: t2embapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: T2embed.lib
req.dll: T2embed.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - T2embed.dll
api_name:
 - TTEnableEmbeddingForFacename
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

