---
UID: NF:winuser.CharPrevExA
title: CharPrevExA function
author: windows-driver-content
description: Retrieves the pointer to the preceding character in a string. This function can handle strings consisting of either single- or multi-byte characters.
old-location: menurc\charprevexa.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\charprevexa.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: CP_ACP, CP_MACCP, CP_OEMCP, CharPrevExA, CharPrevExA function [Menus and Other Resources], _win32_CharPrevExA, _win32_charprevexa_cpp, menurc.charprevexa, winui._win32_charprevexa, winuser/CharPrevExA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CharPrevExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	API-MS-Win-Core-Stringansi-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-user32-l1-1-0.dll
-	API-MS-Win-DownLevel-user32-l1-1-1.dll
api_name:
-	CharPrevExA
-	CharPrevExA
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

