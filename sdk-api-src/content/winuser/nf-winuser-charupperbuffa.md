---
UID: NF:winuser.CharUpperBuffA
title: CharUpperBuffA function
author: windows-sdk-content
description: Converts lowercase characters in a buffer to uppercase characters. The function converts the characters in place.
old-location: menurc\charupperbuff.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\charupperbuff.htm
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: CharUpperBuff, CharUpperBuff function [Menus and Other Resources], CharUpperBuffA, CharUpperBuffW, _win32_CharUpperBuff, _win32_charupperbuff_cpp, menurc.charupperbuff, winui._win32_charupperbuff, winuser/CharUpperBuff, winuser/CharUpperBuffA, winuser/CharUpperBuffW
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
req.unicode-ansi: CharUpperBuffW (Unicode) and CharUpperBuffA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CharUpperBuffA function


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

For an example, see <a href="_win32_Creating_and_Using_a_Temporary_File">Creating and Using a Temporary File</a>. 



<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b67786aa-d629-4d23-b4cb-efb43282ca02">CharLower</a>



<a href="https://msdn.microsoft.com/3a678c1b-76a5-4a08-8a13-dfc400492bba">CharLowerBuff</a>



<a href="https://msdn.microsoft.com/4a101fb6-8b90-479b-93dc-3f768e9b952a">CharUpper</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>
 

 

