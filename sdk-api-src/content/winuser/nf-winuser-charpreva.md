---
UID: NF:winuser.CharPrevA
title: CharPrevA function
author: windows-sdk-content
description: Retrieves a pointer to the preceding character in a string. This function can handle strings consisting of either single- or multi-byte characters.
old-location: menurc\charprev.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\charprev.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CharPrev, CharPrev function [Menus and Other Resources], CharPrevA, CharPrevW, _win32_CharPrev, _win32_charprev_cpp, menurc.charprev, winui._win32_charprev, winuser/CharPrev, winuser/CharPrevA, winuser/CharPrevW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AR_STATE, *PAR_STATE
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



When called as an ANSI function, <b>CharPrev</b> uses the system default code-page, whereas <a href="https://msdn.microsoft.com/887a11c3-57fb-4407-a842-957e20931610">CharPrevExA</a> specifies a code-page to use.


			This function works with default "user" expectations of characters when dealing with diacritics. For example:
A string that contains U+0061 U+030a "LATIN SMALL LETTER A" + COMBINING RING ABOVE" — which looks like "å", will advance two code points, not one.
A string that contains U+0061 U+0301 U+0302 U+0303 U+0304 — which looks like "a´^~¯", will advance five code points, not one,
and so on.
			




## -see-also




<a href="https://msdn.microsoft.com/23be5ba3-bc2e-4c5b-95d2-b36dc24007ae">CharNext</a>



<a href="https://msdn.microsoft.com/0501744a-83a5-4ac4-b934-3e794fe940c0">CharNextExA</a>



<a href="https://msdn.microsoft.com/887a11c3-57fb-4407-a842-957e20931610">CharPrevExA</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>
 

 

