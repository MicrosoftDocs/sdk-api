---
UID: NF:winuser.CharNextExA
title: CharNextExA function (winuser.h)
description: Retrieves the pointer to the next character in a string. This function can handle strings consisting of either single- or multi-byte characters.
helpviewer_keywords: ["CP_ACP","CP_MACCP","CP_OEMCP","CharNextExA","CharNextExA function [Menus and Other Resources]","_win32_CharNextExA","_win32_charnextexa_cpp","menurc.charnextexa","winui._win32_charnextexa","winuser/CharNextExA"]
old-location: menurc\charnextexa.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\charnextexa.htm
ms.date: 12/05/2018
ms.keywords: CP_ACP, CP_MACCP, CP_OEMCP, CharNextExA, CharNextExA function [Menus and Other Resources], _win32_CharNextExA, _win32_charnextexa_cpp, menurc.charnextexa, winui._win32_charnextexa, winuser/CharNextExA
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CharNextExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CharNextExA
 - winuser/CharNextExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-Core-Stringansi-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-user32-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-1.dll
api_name:
 - CharNextExA
 - CharNextExA
---

# CharNextExA function


## -description

Retrieves the pointer to the next character in a string. This function can handle strings consisting of either single- or multi-byte characters.

## -parameters

### -param CodePage [in]

Type: <b>WORD</b>

The identifier of the code page to use to check lead-byte ranges. Can be one of the code-page values provided in <a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a>, or one of the following predefined values. 

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

<b>CharNextExA</b> specifies a code-page to use, whereas <a href="/windows/desktop/api/winuser/nf-winuser-charnexta">CharNext</a> (if called as an ANSI function) uses the system default code-page.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-charnexta">CharNext</a>



<a href="/windows/desktop/api/winuser/nf-winuser-charprevexa">CharPrevExA</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/menurc/strings">Strings</a>