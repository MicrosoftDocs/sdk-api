---
UID: NF:winuser.wvsprintfW
title: wvsprintfW function
author: windows-sdk-content
description: Writes formatted data to the specified buffer using a pointer to a list of arguments.
old-location: menurc\wvsprintf.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\wvsprintf.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_win32_wvsprintf, _win32_wvsprintf_cpp, menurc.wvsprintf, winui._win32_wvsprintf, winuser/wvsprintf, winuser/wvsprintfA, winuser/wvsprintfW, wvsprintf, wvsprintf function [Menus and Other Resources], wvsprintfA, wvsprintfW"
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
req.unicode-ansi: wvsprintfW (Unicode) and wvsprintfA (ANSI)
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
api_name:
 - wvsprintf
 - wvsprintfA
 - wvsprintfW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- wvsprintfW
: 
---

# wvsprintfW function


## -description


Writes formatted data to the specified buffer using a pointer to a list of arguments. The items pointed to by the argument list are converted and copied to an output buffer according to the corresponding format specification in the format-control string. The function appends a terminating null character to the characters it writes, but the return value does not include the terminating null character in its character count.
<div class="alert"><b>Warning</b>  Do not use. Consider using one of the following functions instead: <a href="https://msdn.microsoft.com/d6985910-65be-4b68-b410-026cef66c651">StringCbVPrintf</a>, 
				<a href="https://msdn.microsoft.com/36f77c17-6244-4357-9361-a04118fcd820">StringCbVPrintfEx</a>, <a href="https://msdn.microsoft.com/82cc5a7c-e4c5-4a88-9bb5-d3f02dc3d7f5">StringCchVPrintf</a>, or
				<a href="https://msdn.microsoft.com/07b4eb68-2b50-4c66-af1a-13cc57144e3a">StringCchVPrintfEx</a>. See Security Considerations.</div><div> </div>

## -parameters




### -param arg1 [out]

Type: <b>LPTSTR</b>

The buffer that is to receive the formatted output. The maximum size of the buffer is 1,024 bytes.


### -param arg2 [in]

Type: <b>LPCTSTR</b>

The format-control specifications. In addition to ordinary ASCII characters, a format specification for each argument appears in this string. For more information about the format specification, see the <a href="https://msdn.microsoft.com/5f373cb3-8cb9-4516-8a18-8971bb430d42">wsprintf</a> function.


### -param arglist [in]

Type: <b>va_list</b>

Each element of this list specifies an argument for the format-control string. The number, type, and interpretation of the arguments depend on the corresponding format-control specifications in the 
					<i>lpFmt</i> parameter.


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the number of characters stored in the buffer, not counting the terminating null character.

If the function fails, the return value is less than the length of the expected output. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The function copies the format-control string into the output buffer character by character, starting with the first character in the string. When it encounters a format specification in the string, the function retrieves the value of the next available argument (starting with the first argument in the list), converts that value into the specified format, and copies the result to the output buffer. The function continues to copy characters and expand format specifications in this way until it reaches the end of the format-control string. If there are more arguments than format specifications, the extra arguments are ignored. If there are not enough arguments for all of the format specifications, the results are undefined.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/224c8840-06c6-4144-8f23-8705ac8ef887">StringCbPrintf</a>



<a href="https://msdn.microsoft.com/525e1fb5-9dfd-4ec2-a4af-9b9e198b6e17">StringCbPrintfEx</a>



<a href="https://msdn.microsoft.com/d6985910-65be-4b68-b410-026cef66c651">StringCbVPrintf</a>



<a href="https://msdn.microsoft.com/36f77c17-6244-4357-9361-a04118fcd820">StringCbVPrintfEx</a>



<a href="https://msdn.microsoft.com/9eaafe87-04da-4273-babb-b16d26bfdf70">StringCchPrintf</a>



<a href="https://msdn.microsoft.com/e3904cd0-fcb9-4b54-9895-513a95f4a6f7">StringCchPrintfEx</a>



<a href="https://msdn.microsoft.com/82cc5a7c-e4c5-4a88-9bb5-d3f02dc3d7f5">StringCchVPrintf</a>



<a href="https://msdn.microsoft.com/07b4eb68-2b50-4c66-af1a-13cc57144e3a">StringCchVPrintfEx</a>



<a href="https://msdn.microsoft.com/f2cb0888-b245-448c-9910-a634312aff67">Strings</a>



<a href="https://msdn.microsoft.com/5f373cb3-8cb9-4516-8a18-8971bb430d42">wsprintf</a>
 

 

