---
UID: NF:winuser.wvsprintfW
title: wvsprintfW function
author: windows-sdk-content
description: Writes formatted data to the specified buffer using a pointer to a list of arguments.
old-location: menurc\wvsprintf.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\wvsprintf.htm
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: "_win32_wvsprintf, _win32_wvsprintf_cpp, menurc.wvsprintf, winui._win32_wvsprintf, winuser/wvsprintf, winuser/wvsprintfA, winuser/wvsprintfW, wvsprintf, wvsprintf function [Menus and Other Resources], wvsprintfA, wvsprintfW"
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
req.unicode-ansi: wvsprintfW (Unicode) and wvsprintfA (ANSI)
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
 - wvsprintf
 - wvsprintfA
 - wvsprintfW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# wvsprintfW function


## -description


Writes formatted data to the specified buffer using a pointer to a list of arguments. The items pointed to by the argument list are converted and copied to an output buffer according to the corresponding format specification in the format-control string. The function appends a terminating null character to the characters it writes, but the return value does not include the terminating null character in its character count.
<div class="alert"><b>Warning</b>  Do not use. Consider using one of the following functions instead: <a href="https://msdn.microsoft.com/library/ms647514(v=VS.85).aspx">StringCbVPrintf</a>, 
				<a href="https://msdn.microsoft.com/library/ms647516(v=VS.85).aspx">StringCbVPrintfEx</a>, <a href="https://msdn.microsoft.com/library/ms647546(v=VS.85).aspx">StringCchVPrintf</a>, or
				<a href="https://msdn.microsoft.com/library/ms647548(v=VS.85).aspx">StringCchVPrintfEx</a>. See Security Considerations.</div><div> </div>

## -parameters




### -param param

TBD


### -param arglist [in]

Type: <b>va_list</b>

Each element of this list specifies an argument for the format-control string. The number, type, and interpretation of the arguments depend on the corresponding format-control specifications in the 
					<i>lpFmt</i> parameter.


#### - lpFmt [in]

Type: <b>LPCTSTR</b>

The format-control specifications. In addition to ordinary ASCII characters, a format specification for each argument appears in this string. For more information about the format specification, see the <a href="https://msdn.microsoft.com/library/ms647550(v=VS.85).aspx">wsprintf</a> function.


#### - lpOutput [out]

Type: <b>LPTSTR</b>

The buffer that is to receive the formatted output. The maximum size of the buffer is 1,024 bytes.


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the number of characters stored in the buffer, not counting the terminating null character.

If the function fails, the return value is less than the length of the expected output. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The function copies the format-control string into the output buffer character by character, starting with the first character in the string. When it encounters a format specification in the string, the function retrieves the value of the next available argument (starting with the first argument in the list), converts that value into the specified format, and copies the result to the output buffer. The function continues to copy characters and expand format specifications in this way until it reaches the end of the format-control string. If there are more arguments than format specifications, the extra arguments are ignored. If there are not enough arguments for all of the format specifications, the results are undefined.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms647510(v=VS.85).aspx">StringCbPrintf</a>



<a href="https://msdn.microsoft.com/library/ms647513(v=VS.85).aspx">StringCbPrintfEx</a>



<a href="https://msdn.microsoft.com/library/ms647514(v=VS.85).aspx">StringCbVPrintf</a>



<a href="https://msdn.microsoft.com/library/ms647516(v=VS.85).aspx">StringCbVPrintfEx</a>



<a href="https://msdn.microsoft.com/library/ms647541(v=VS.85).aspx">StringCchPrintf</a>



<a href="https://msdn.microsoft.com/library/ms647543(v=VS.85).aspx">StringCchPrintfEx</a>



<a href="https://msdn.microsoft.com/library/ms647546(v=VS.85).aspx">StringCchVPrintf</a>



<a href="https://msdn.microsoft.com/library/ms647548(v=VS.85).aspx">StringCchVPrintfEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>



<a href="https://msdn.microsoft.com/library/ms647550(v=VS.85).aspx">wsprintf</a>
 

 

