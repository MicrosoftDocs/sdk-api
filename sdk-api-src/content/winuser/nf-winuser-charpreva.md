---
UID: NF:winuser.CharPrevA
title: CharPrevA function (winuser.h)
author: windows-sdk-content
description: Retrieves a pointer to the preceding character in a string. This function can handle strings consisting of either single- or multi-byte characters.
old-location: menurc\charprev.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\charprev.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CharPrev, CharPrev function [Menus and Other Resources], CharPrevA, CharPrevW, _win32_CharPrev, _win32_charprev_cpp, menurc.charprev, winui._win32_charprev, winuser/CharPrev, winuser/CharPrevA, winuser/CharPrevW
ms.topic: function
f1_keywords: ["winuser/CharPrev"]
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CharPrevW (Unicode) and CharPrevA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-Core-String-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-String-l2-1-1.dll
 - API-MS-Win-Core-Stringansi-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-1.dll
api_name:
 - CharPrev
 - CharPrevA
 - CharPrevW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CharPrevA function


## -description


Retrieves a pointer to the preceding character in a string. This function can handle strings consisting of either single- or multi-byte characters.


## -parameters




### -param lpszStart [in]

Type: <b>LPCTSTR</b>

The beginning of the string.


### -param lpszCurrent [in]

Type: <b>LPCTSTR</b>

A character in a null-terminated string.


## -returns



Type: <b>LPTSTR</b>

The return value is a pointer to the preceding character in the string, or to the first character in the string if the 
						<i>lpszCurrent</i> parameter equals the 
						<i>lpszStart</i> parameter.




## -remarks



When called as an ANSI function, <b>CharPrev</b> uses the system default code-page, whereas <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-charprevexa">CharPrevExA</a> specifies a code-page to use.

This function works with default "user" expectations of characters when dealing with diacritics. For example:
A string that contains U+0061 U+030a "LATIN SMALL LETTER A" + COMBINING RING ABOVE" — which looks like "å", will advance two code points, not one.
A string that contains U+0061 U+0301 U+0302 U+0303 U+0304 — which looks like "a´^~¯", will advance five code points, not one,
and so on.
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-charnexta">CharNext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-charnextexa">CharNextExA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-charprevexa">CharPrevExA</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/strings">Strings</a>
 

 

