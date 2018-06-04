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

# CharPrevExA function


## -description


Retrieves the pointer to the preceding character in a string. This function can handle strings consisting of either single- or multi-byte characters.


## -parameters




### -param CodePage [in]

Type: <b>WORD</b>

The identifier of the code page to use to check lead-byte ranges. Can be one of the code-page values provided in <a href="https://msdn.microsoft.com/5d6fc86a-f205-4d14-bb7c-ecd71682e0fe">Code Page Identifiers</a>,  or one of the following predefined values.

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
 


### -param lpStart [in]

Type: <b>LPCSTR</b>

The beginning of the string.


### -param lpCurrentChar [in]

Type: <b>LPCSTR</b>

A character in a null-terminated string.


### -param dwFlags [in]

Type: <b>DWORD</b>

This parameter is reserved and must be zero.


## -returns



Type: <b>LPSTR</b>

The return value is a pointer to the preceding character in the string, or to the first character in the string if the 
						<i>lpCurrentChar</i> parameter equals the 
						<i>lpStart</i> parameter. 




## -remarks



<b>CharPrevExA</b> specifies a code-page to use, whereas <a href="https://msdn.microsoft.com/f1599f24-2a6f-4887-8712-302631fee313">CharPrev</a> (if called as an ANSI function) uses the system default code-page.




## -see-also




<a href="https://msdn.microsoft.com/0501744a-83a5-4ac4-b934-3e794fe940c0">CharNextExA</a>



<a href="https://msdn.microsoft.com/f1599f24-2a6f-4887-8712-302631fee313">CharPrev</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>
 

 

