---
UID: NF:winbase.lstrcpyW
title: lstrcpyW function
author: windows-sdk-content
description: Copies a string to a buffer.
old-location: menurc\lstrcpy.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrcpy.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: "_win32_lstrcpy, _win32_lstrcpy_cpp, lstrcpy, lstrcpy function [Menus and Other Resources], lstrcpyA, lstrcpyW, menurc.lstrcpy, winbase/lstrcpy, winbase/lstrcpyA, winbase/lstrcpyW, winui._win32_lstrcpy"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lstrcpyW (Unicode) and lstrcpyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
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
api_name:
 - lstrcpy
 - lstrcpyA
 - lstrcpyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lstrcpyW function


## -description


Copies a string to a buffer.
<div class="alert"><b>Warning</b>  Do not use. Consider using <a href="https://msdn.microsoft.com/9cbf6ce6-ef45-4bb9-bc1f-a55db399d34f">StringCchCopy</a> instead. See Remarks.</div><div> </div>

## -parameters




### -param lpString1 [out]

Type: <b>LPTSTR</b>

A buffer to receive the contents of the string pointed to by the 
					<i>lpString2</i> parameter. 
					The buffer must be large enough to contain the string, including the 
					terminating null character. 


### -param lpString2 [in]

Type: <b>LPTSTR</b>

The null-terminated string to be copied.


## -returns



Type: <b>LPTSTR</b>

If the function succeeds, the return value is a pointer to the buffer.

If the function fails, the return value is <b>NULL</b> 
                    and <i>lpString1</i> may not be null-terminated.




## -remarks



With a double-byte character set (DBCS) version of the system, this function can be used 
			to copy a DBCS string. 

The <b>lstrcpy</b> function has an 
			undefined behavior if source and destination buffers overlap.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
Using this function incorrectly can compromise the security 
			of your application. This function uses structured exception handling (SEH) to catch 
			access violations and other errors. When this function catches SEH errors, it returns 
			<b>NULL</b> without null-terminating the string and without notifying the 
			caller of the error. The caller is not safe to assume that insufficient space is 
			the error condition.

<i>lpString1</i> must be large enough to hold <i>lpString2</i> 
			and the closing '\0', otherwise a buffer overrun may occur.

Buffer overflow situations are the cause of many security problems in applications and 
			can cause a denial of service attack against the application if an access violation occurs. 
			In the worst case, a buffer overrun may allow an attacker to inject executable code into 
			your process, especially if <i>lpString1</i> is a stack-based buffer.

Consider using <a href="https://msdn.microsoft.com/9cbf6ce6-ef45-4bb9-bc1f-a55db399d34f">StringCchCopy</a> instead; use either 
				<code>StringCchCopy(buffer, sizeof(buffer)/sizeof(buffer[0]), src);</code>, 
				being aware that <code>buffer</code> must not be a pointer or 
				use <code>StringCchCopy(buffer, ARRAYSIZE(buffer), src);</code>, 
				being aware that, when copying to a pointer, the caller is responsible for 
				passing in the size of the pointed-to memory in characters. 




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/00c99f3e-106b-46a2-afae-517b32b7a960">StringCbCopy</a>



<a href="https://msdn.microsoft.com/28750482-a0ba-43e1-b433-2c850feef051">StringCbCopyEx</a>



<a href="https://msdn.microsoft.com/4b97de2a-c8bb-423e-8765-a7f20e6fc61c">StringCbCopyN</a>



<a href="https://msdn.microsoft.com/0ef55f41-000c-475a-8227-66df352366fb">StringCbCopyNEx</a>



<a href="https://msdn.microsoft.com/9cbf6ce6-ef45-4bb9-bc1f-a55db399d34f">StringCchCopy</a>



<a href="https://msdn.microsoft.com/0965b0f6-9588-4944-98d8-3aca3a3029fc">StringCchCopyEx</a>



<a href="https://msdn.microsoft.com/5803c6fa-d1ae-4c3b-8627-162039e8c31f">StringCchCopyN</a>



<a href="https://msdn.microsoft.com/228ddd78-9747-4a9a-b936-abfba6ff2940">StringCchCopyNEx</a>



<a href="https://msdn.microsoft.com/f2cb0888-b245-448c-9910-a634312aff67">Strings</a>



<a href="https://msdn.microsoft.com/e7b6ac43-ef24-4121-bb4e-a01232b034ad">lstrcmp</a>



<a href="https://msdn.microsoft.com/7edd4896-04d3-4b71-9ce6-d64149d683e0">lstrcmpi</a>



<a href="https://msdn.microsoft.com/0024853f-3a1f-4742-bc5e-f0ca89e23f3a">lstrlen</a>
 

 

