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

# SHStripMneumonicW function


## -description


<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Removes the mnemonic marker from a string.


## -parameters




### -param pszMenu [in, out]

Type: <b>LPTSTR*</b>

A pointer to the null-terminated string that contains the mnemonic marker.


## -returns



Type: <b>TCHAR</b>

Returns the mnemonic character, if one was found. Otherwise, returns 0.




## -remarks



The term "mnemonic" is misspelled in the function name.

The function supports the following mnemonic formats.
        
                

<table class="clsStd">
<tr>
<th>Input String</th>
<th>Output String</th>
<th>Mnemonic Character</th>
<th>Remarks</th>
</tr>
<tr>
<td>"Str&amp;ing"</td>
<td>"String"</td>
<td>'i'</td>
<td>None.</td>
</tr>
<tr>
<td>"String (&amp;S)"</td>
<td>"String"</td>
<td>'S'</td>
<td>Supported only by the Unicode version of this function. Requires Windows XP or later.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fe412280-d797-4abd-8a29-107a9cd96145">DrawText</a>
 

 

