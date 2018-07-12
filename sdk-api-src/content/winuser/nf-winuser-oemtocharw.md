---
UID: NF:winuser.OemToCharW
title: OemToCharW function
author: windows-sdk-content
description: Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.Warning  Do not use.
old-location: menurc\oemtochar.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\oemtochar.htm
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: OemToChar, OemToChar function [Menus and Other Resources], OemToCharA, OemToCharW, _win32_OemToChar, _win32_oemtochar_cpp, menurc.oemtochar, winui._win32_oemtochar, winuser/OemToChar, winuser/OemToCharA, winuser/OemToCharW
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
req.unicode-ansi: OemToCharW (Unicode) and OemToCharA (ANSI)
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
api_name:
 - OemToChar
 - OemToCharA
 - OemToCharW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OemToCharW function


## -description


Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.
<div class="alert"><b>Warning</b>  Do not use. See Security Considerations.</div><div> </div>

## -parameters




### -param pSrc

TBD


### -param pDst

TBD




#### - lpszDst [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the translated string. If the <b>OemToChar</b> function is being used as an ANSI function, the string can be translated in place by setting the 
					<i>lpszDst</i> parameter to the same address as the 
					<i>lpszSrc</i> parameter. This cannot be done if <b>OemToChar</b> is being used as a wide-character function.


#### - lpszSrc [in]

Type: <b>LPCSTR</b>

A null-terminated string of characters from the OEM-defined character set. 


## -returns



Type: <b>BOOL</b>

The return value is always nonzero except when you pass the same address to 
						<i>lpszSrc</i> and 
						<i>lpszDst</i> in the wide-character version of the function. In this case the function returns zero and 
						<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INVALID_ADDRESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms647473(v=VS.85).aspx">CharToOem</a>



<a href="https://msdn.microsoft.com/library/Dd319646(v=VS.85).aspx">CharToOemBuff</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms647494(v=VS.85).aspx">OemToCharBuff</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>
 

 

