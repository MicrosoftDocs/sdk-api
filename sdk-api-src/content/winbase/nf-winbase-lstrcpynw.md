---
UID: NF:winbase.lstrcpynW
title: lstrcpynW function
author: windows-sdk-content
description: Copies a specified number of characters from a source string into a buffer.Warning  Do not use.
old-location: menurc\lstrcpyn.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrcpyn.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "_win32_lstrcpyn, _win32_lstrcpyn_cpp, lstrcpyn, lstrcpyn function [Menus and Other Resources], lstrcpynA, lstrcpynW, menurc.lstrcpyn, winbase/lstrcpyn, winbase/lstrcpynA, winbase/lstrcpynW, winui._win32_lstrcpyn"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lstrcpynW (Unicode) and lstrcpynA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-String-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-String-Obsolete-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - lstrcpyn
 - lstrcpynA
 - lstrcpynW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# lstrcpynW function


## -description


Copies a specified number of characters from a source string into a buffer.
<div class="alert"><b>Warning</b>  Do not use. Consider using <a href="https://msdn.microsoft.com/9cbf6ce6-ef45-4bb9-bc1f-a55db399d34f">StringCchCopy</a> instead. See Remarks.</div><div> </div>

## -parameters




### -param lpString1 [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the copied characters. The buffer 
				must be large enough to contain the number of <b>TCHAR</b> values 
				specified by <i>iMaxLength</i>, including room 
				for a terminating null character.


### -param lpString2 [in]

Type: <b>LPCTSTR</b>

The source string from which the function is to copy characters.


### -param iMaxLength [in]

Type: <b>int</b>

The number of <b>TCHAR</b> values to be copied from the 
				string pointed to by <i>lpString2</i> into the 
				buffer pointed to by <i>lpString1</i>, including 
				a terminating null character. 


## -returns



Type: <b>LPTSTR</b>

If the function succeeds, the return value is a pointer to the buffer. 
				The function can succeed even if the source string is greater than 
				<i>iMaxLength</i> characters.

If the function fails, the return value is <b>NULL</b> 
                    and <i>lpString1</i> may not be null-terminated.




## -remarks



The buffer pointed to by <i>lpString1</i> must 
			be large enough to include a terminating null character, and the string length 
			value specified by <i>iMaxLength</i> includes room 
			for a terminating null character. 

The <b>lstrcpyn</b> function has an undefined behavior if source 
    and destination buffers overlap.

<h3><a id="Security_Warning"></a><a id="security_warning"></a><a id="SECURITY_WARNING"></a>Security Warning</h3>
Using this function incorrectly can compromise the security 
			of your application. This function uses structured exception handling (SEH) to catch 
			access violations and other errors. When this function catches SEH errors, it returns 
			<b>NULL</b> without null-terminating the string and without notifying the 
			caller of the error. The caller is not safe to assume that insufficient space is 
			the error condition.

If the buffer pointed to by <i>lpString1</i> is not large 
			enough to contain the copied string, a buffer overrun can occur. When copying an entire 
			string, note that <b>sizeof</b> returns the number of bytes. 
			For example, if <i>lpString1</i> points to a buffer 
			<i>szString1</i> which is declared as 
			<code>TCHAR szString[100]</code>, then sizeof(szString1) gives the size of 
			the buffer in bytes rather than <b>WCHAR</b>, which could lead to a buffer 
			overflow for the Unicode version of the function. 

Buffer overflow situations are the cause 
			of many security problems in applications and can cause a denial of service attack against 
			the application if an access violation occurs. In the worst case, a buffer overrun may 
			allow an attacker to inject executable code into your process, especially if 
			<i>lpString1</i> is a stack-based buffer.

Using <code>sizeof(szString1)/sizeof(szString1[0])</code> 
				gives the proper size of the buffer. 

Consider using <a href="https://msdn.microsoft.com/9cbf6ce6-ef45-4bb9-bc1f-a55db399d34f">StringCchCopy</a> instead; use either 
				<code>StringCchCopy(buffer, sizeof(buffer)/sizeof(buffer[0]), src);</code>, 
				being aware that <code>buffer</code> must not be a pointer or 
				use <code>StringCchCopy(buffer, ARRAYSIZE(buffer), src);</code>, 
				being aware that, when copying to a pointer, the caller is responsible for 
				passing in the size of the pointed-to memory in characters. 

Review <a href="https://www.bing.com/search?q=Security+Considerations:+Windows+User+Interface">Security Considerations: Windows User Interface</a> before continuing.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/00c99f3e-106b-46a2-afae-517b32b7a960">StringCbCopy</a>



<a href="https://msdn.microsoft.com/28750482-a0ba-43e1-b433-2c850feef051">StringCbCopyEx</a>



<a href="https://msdn.microsoft.com/4b97de2a-c8bb-423e-8765-a7f20e6fc61c">StringCbCopyN</a>



<a href="https://msdn.microsoft.com/0ef55f41-000c-475a-8227-66df352366fb">StringCbCopyNEx</a>



<a href="https://msdn.microsoft.com/a1aa834c-53e7-4321-9db4-86f32ef31dc4">StringCbLength</a>



<a href="https://msdn.microsoft.com/9cbf6ce6-ef45-4bb9-bc1f-a55db399d34f">StringCchCopy</a>



<a href="https://msdn.microsoft.com/0965b0f6-9588-4944-98d8-3aca3a3029fc">StringCchCopyEx</a>



<a href="https://msdn.microsoft.com/5803c6fa-d1ae-4c3b-8627-162039e8c31f">StringCchCopyN</a>



<a href="https://msdn.microsoft.com/228ddd78-9747-4a9a-b936-abfba6ff2940">StringCchCopyNEx</a>



<a href="https://msdn.microsoft.com/4b29469a-e9a8-4309-9d19-db74a8bd6038">StringCchLength</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>



<a href="https://msdn.microsoft.com/e7b6ac43-ef24-4121-bb4e-a01232b034ad">lstrcmp</a>



<a href="https://msdn.microsoft.com/7edd4896-04d3-4b71-9ce6-d64149d683e0">lstrcmpi</a>



<a href="https://msdn.microsoft.com/0024853f-3a1f-4742-bc5e-f0ca89e23f3a">lstrlen</a>
 

 

