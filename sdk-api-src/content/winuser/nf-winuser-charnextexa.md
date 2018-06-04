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

# CharNextExA function


## -description


Retrieves the pointer to the next character in a string. This function can handle strings consisting of either single- or multi-byte characters.


## -parameters




### -param CodePage [in]

Type: <b>WORD</b>

The identifier of the code page to use to check lead-byte ranges. Can be one of the code-page values provided in <a href="https://msdn.microsoft.com/5d6fc86a-f205-4d14-bb7c-ecd71682e0fe">Code Page Identifiers</a>, or one of the following predefined values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CP_ACP"></a><a id="cp_acp"></a><dl>
<dt><b>CP_ACP</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Use system default ANSI code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_MACCP"></a><a id="cp_maccp"></a><dl>
<dt><b>CP_MACCP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
 Use the system default Macintosh code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_OEMCP"></a><a id="cp_oemcp"></a><dl>
<dt><b>CP_OEMCP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Use system default OEM code page.

</td>
</tr>
</table>
 


### -param lpCurrentChar [in]

Type: <b>LPCSTR</b>

A character in a null-terminated string.


### -param dwFlags [in]

Type: <b>DWORD</b>

This parameter is reserved and must be 0.


## -returns



Type: <b>LPSTR</b>

The return value is a pointer to the next character in the string, or to the terminating null character if at the end of the string.

If 
						<i>lpCurrentChar</i> points to the terminating null character, the return value is equal to 
						<i>lpCurrentChar</i>.




## -remarks



<b>CharNextExA</b> specifies a code-page to use, whereas <a href="https://msdn.microsoft.com/23be5ba3-bc2e-4c5b-95d2-b36dc24007ae">CharNext</a> (if called as an ANSI function) uses the system default code-page.




## -see-also




<a href="https://msdn.microsoft.com/23be5ba3-bc2e-4c5b-95d2-b36dc24007ae">CharNext</a>



<a href="https://msdn.microsoft.com/887a11c3-57fb-4407-a842-957e20931610">CharPrevExA</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>
 

 

