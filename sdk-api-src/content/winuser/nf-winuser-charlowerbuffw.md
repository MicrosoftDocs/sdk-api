---
UID: NF:winuser.CharLowerBuffW
title: CharLowerBuffW function
author: windows-sdk-content
description: Converts uppercase characters in a buffer to lowercase characters. The function converts the characters in place.
old-location: menurc\charlowerbuff.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\charlowerbuff.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CharLowerBuff, CharLowerBuff function [Menus and Other Resources], CharLowerBuffA, CharLowerBuffW, _win32_CharLowerBuff, _win32_charlowerbuff_cpp, menurc.charlowerbuff, winui._win32_charlowerbuff, winuser/CharLowerBuff, winuser/CharLowerBuffA, winuser/CharLowerBuffW
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CharLowerBuffW
: 
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



Note that <b>CharLowerBuff</b> always maps uppercase I to lowercase I  ("i"), even when the current language is Turkish or Azerbaijani. If you need a function that is linguistically sensitive in this respect, call <a href="https://msdn.microsoft.com/84dda2cd-cbf9-45e9-b18c-7dea0b5bc991">LCMapSting</a>.

Conversion to Unicode in the ANSI version of the function is done with the system default locale in all cases.


#### Examples

For an example, see "Creating a Spell Dialog Box" in <a href="https://msdn.microsoft.com/en-us/library/Bb775794(v=VS.85).aspx">Using Combo Boxes</a>. 



<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms647467(v=VS.85).aspx">CharLower</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647474(v=VS.85).aspx">CharUpper</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647475(v=VS.85).aspx">CharUpperBuff</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646979(v=VS.85).aspx">Strings</a>
 

 

