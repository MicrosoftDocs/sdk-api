---
UID: NF:winuser.CharUpperW
title: CharUpperW function (winuser.h)
author: windows-sdk-content
description: Converts a character string or a single character to uppercase. If the operand is a character string, the function converts the characters in place.
old-location: menurc\charupper.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\charupper.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CharUpper, CharUpper function [Menus and Other Resources], CharUpperA, CharUpperW, _win32_CharUpper, _win32_charupper_cpp, menurc.charupper, winui._win32_charupper, winuser/CharUpper, winuser/CharUpperA, winuser/CharUpperW
ms.topic: function
f1_keywords: ["winuser/CharUpper"]
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CharUpperW (Unicode) and CharUpperA (ANSI)
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
 - API-MS-Win-deprecated-apis-Obsolete-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-1.dll
api_name:
 - CharUpper
 - CharUpperA
 - CharUpperW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CharUpperW function


## -description


Converts a character string or a single character to uppercase. If the operand is a character string, the function converts the characters in place. 


## -parameters




### -param lpsz [in, out]

Type: <b>LPTSTR</b>

A null-terminated string, or a single character. If the high-order word of this parameter is zero, the low-order word must contain a single character to be converted.


## -returns



Type: <b>LPTSTR</b>

If the operand is a character string, the function returns a pointer to the converted string. Because the string is converted in place, the return value is equal to 
						<i>lpsz</i>. 

If the operand is a single character, the return value is a 32-bit value whose high-order word is zero, and low-order word contains the converted character. 

There is no indication of success or failure. Failure is rare. There is no extended error information for this function; do not call 
						<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Note that <b>CharUpper</b> always maps lowercase I ("i") to uppercase I, even when the current language is Turkish or Azerbaijani. If you need a function that is linguistically sensitive in this respect, call <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.

Conversion to Unicode in the ANSI version of the function is done with the system default locale in all cases.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-charlowera">CharLower</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/f">CharLowerBuff</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-charupperbuffa">CharUpperBuff</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/strings">Strings</a>
 

 

