---
UID: NF:winuser.CharUpperBuffW
title: CharUpperBuffW function
author: windows-sdk-content
description: Converts lowercase characters in a buffer to uppercase characters. The function converts the characters in place.
old-location: menurc\charupperbuff.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\charupperbuff.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CharUpperBuff, CharUpperBuff function [Menus and Other Resources], CharUpperBuffA, CharUpperBuffW, _win32_CharUpperBuff, _win32_charupperbuff_cpp, menurc.charupperbuff, winui._win32_charupperbuff, winuser/CharUpperBuff, winuser/CharUpperBuffA, winuser/CharUpperBuffW
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
req.unicode-ansi: CharUpperBuffW (Unicode) and CharUpperBuffA (ANSI)
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
 - CharUpperBuff
 - CharUpperBuffA
 - CharUpperBuffW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CharUpperBuffW
: 
---

# CharUpperBuffW function


## -description


Converts lowercase characters in a buffer to uppercase characters. The function converts the characters in place. 


## -parameters




### -param lpsz [in, out]

Type: <b>LPTSTR</b>

A buffer containing one or more characters to be processed.


### -param cchLength [in]

Type: <b>DWORD</b>

The size, in characters, of the buffer pointed to by <i>lpsz</i>.

The function examines each character, and converts lowercase characters to uppercase characters. The function examines the number of characters indicated by 
					<i>cchLength</i>, even if one or more characters are null characters. 


## -returns



Type: <b>DWORD</b>

The return value is the number of 
						characters processed.

For example, if <b>CharUpperBuff</b>("Zenith of API Sets", 10) succeeds, the return value is 10.




## -remarks



Note that <b>CharUpperBuff</b> always maps lowercase I ("i") to uppercase I, even when the current language is Turkish or Azerbaijani. If you need a function that is linguistically sensitive in this respect, call <a href="https://msdn.microsoft.com/84dda2cd-cbf9-45e9-b18c-7dea0b5bc991">LCMapString</a>.

Conversion to Unicode in the ANSI version of the function is done with the system default locale in all cases.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/Aa363875(v=VS.85).aspx">Creating and Using a Temporary File</a>. 



<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms647467(v=VS.85).aspx">CharLower</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647468(v=VS.85).aspx">CharLowerBuff</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647474(v=VS.85).aspx">CharUpper</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646979(v=VS.85).aspx">Strings</a>
 

 

