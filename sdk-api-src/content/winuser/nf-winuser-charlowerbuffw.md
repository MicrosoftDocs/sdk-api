---
UID: NF:winuser.CharLowerBuffW
title: CharLowerBuffW function (winuser.h)
description: Converts uppercase characters in a buffer to lowercase characters. The function converts the characters in place.helpviewer_keywords: ["CharLowerBuff","CharLowerBuff function [Menus and Other Resources]","CharLowerBuffA","CharLowerBuffW","_win32_CharLowerBuff","_win32_charlowerbuff_cpp","menurc.charlowerbuff","winui._win32_charlowerbuff","winuser/CharLowerBuff","winuser/CharLowerBuffA","winuser/CharLowerBuffW"]
old-location: menurc\charlowerbuff.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\charlowerbuff.htm
ms.date: 12/05/2018
ms.keywords: CharLowerBuff, CharLowerBuff function [Menus and Other Resources], CharLowerBuffA, CharLowerBuffW, _win32_CharLowerBuff, _win32_charlowerbuff_cpp, menurc.charlowerbuff, winui._win32_charlowerbuff, winuser/CharLowerBuff, winuser/CharLowerBuffA, winuser/CharLowerBuffW
f1_keywords:
- winuser/CharLowerBuff
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CharLowerBuffW (Unicode) and CharLowerBuffA (ANSI)
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
- CharLowerBuff
- CharLowerBuffA
- CharLowerBuffW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CharLowerBuffW function


## -description


Converts uppercase characters in a buffer to lowercase characters. The function converts the characters in place. 


## -parameters




### -param lpsz [in, out]

Type: <b>LPTSTR</b>

A buffer containing one or more characters to be processed.


### -param cchLength [in]

Type: <b>DWORD</b>

The size, in 
					characters, of the buffer pointed to by 
					<i>lpsz</i>. The function examines each character, and converts uppercase characters to lowercase characters. The function examines the number of 
					characters indicated by 
					<i>cchLength</i>, even if one or more characters are null characters. 


## -returns



Type: <b>DWORD</b>

The return value is the number of 
						characters processed. For example, if <b>CharLowerBuff</b>("Acme of Operating Systems", 10) succeeds, the return value is 10.




## -remarks



Note that <b>CharLowerBuff</b> always maps uppercase I to lowercase I  ("i"), even when the current language is Turkish or Azerbaijani. If you need a function that is linguistically sensitive in this respect, call <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapSting</a>.

Conversion to Unicode in the ANSI version of the function is done with the system default locale in all cases.


#### Examples

For an example, see "Creating a Spell Dialog Box" in <a href="https://docs.microsoft.com/windows/desktop/Controls/using-combo-boxes">Using Combo Boxes</a>. 



<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-charlowera">CharLower</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-charuppera">CharUpper</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-charupperbuffa">CharUpperBuff</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/strings">Strings</a>
 

 

