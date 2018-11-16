---
UID: NF:shlwapi.SHUnicodeToUnicode
title: SHUnicodeToUnicode function
author: windows-sdk-content
description: Copies a Unicode string.
old-location: shell\SHUnicodeToUnicode.htm
tech.root: shell
ms.assetid: 1a208c2d-e627-4aac-9a28-b579c734a2a8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SHUnicodeToUnicode, SHUnicodeToUnicode function [Windows Shell], _win32_SHUnicodeToUnicode, shell.SHUnicodeToUnicode, shlwapi/SHUnicodeToUnicode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-unicodeansi-l1-1-0.dll
api_name:
 - SHUnicodeToUnicode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SHUnicodeToUnicode
: 
---

# SHUnicodeToUnicode function


## -description


<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Copies a Unicode string.


## -parameters




### -param pwzSrc [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string to be copied to the output buffer.


### -param pwzDst [out]

Type: <b>PWSTR</b>

A pointer to an output buffer to receive the copied characters. The buffer must be large enough to contain the number of <b>WCHAR</b> characters specified by <i>cwchBuf</i>, including room for a terminating null character.


### -param cwchBuf

Type: <b>int</b>

The number of <b>WCHAR</b> characters that can be contained by the buffer pointed to by <i>pwzDst</i> parameter. This parameter must be greater than zero.


## -returns



Type: <b>int</b>

Returns the number of <b>WCHAR</b> characters written to the output buffer, including the terminating null character. Returns 0 if unsuccessful.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. For example, if <i>pwzDst</i> buffer is not large enough to contain the number of characters specified by <i>cwchBuf</i>, a buffer overrun can occur. Buffer overruns can cause a denial of service attack against an application if an access violation occurs. In the worst case, a buffer overrun might allow an attacker to inject executable code into your process, especially if <i>pwzDst</i> is a stack-based buffer. When copying an entire string, note that sizeof returns the number of bytes, which is not the correct value to use for the <i>cwchBuf</i> parameter. Instead, use sizeof(pwzDst)/sizeof(WCHAR). Note that this technique assumes that <i>pwzDst</i> is an array, not a pointer. Note also that the function silently truncates the output string  if the buffer is not large enough. This can result in canonicalization or other security vulnerabilities.

If the <i>pwzDst</i> buffer is not large enough to contain the entire converted output string, the string is truncated to fit the buffer. There is no way to detect that the return string has been truncated.  The string will always be null-terminated, even if it has been truncated. This ensures that no more than <i>cwchBuf</i> characters are copied to <i>pwzDst</i>. No attempt is made to avoid truncating the string in the middle of a Unicode surrogate pair.

If the <i>pwzSrc</i> and <i>pwzDst</i> buffers overlap, the function's behavior is undefined.

<div class="alert"><b>Note</b>  Do not assume that the function has not changed any of the characters in the output buffer that follow the string's terminating null character. The contents of the output buffer following the string's terminating null character are undefined, up to and including the last character in the buffer.</div>
<div> </div>
<b>SHTCharToUnicode</b> is defined to be the same as <b>SHUnicodeToUnicode</b>.

<b>SHUnicodeToTChar</b> is defined to be the same as <b>SHUnicodeToUnicode</b>.




## -see-also




<a href="https://msdn.microsoft.com/00c99f3e-106b-46a2-afae-517b32b7a960">StringCbCopy</a>



<a href="https://msdn.microsoft.com/28750482-a0ba-43e1-b433-2c850feef051">StringCbCopyEx</a>



<a href="https://msdn.microsoft.com/4b97de2a-c8bb-423e-8765-a7f20e6fc61c">StringCbCopyN</a>



<a href="https://msdn.microsoft.com/0ef55f41-000c-475a-8227-66df352366fb">StringCbCopyNEx</a>



<a href="https://msdn.microsoft.com/a1aa834c-53e7-4321-9db4-86f32ef31dc4">StringCbLength</a>



<a href="https://msdn.microsoft.com/9cbf6ce6-ef45-4bb9-bc1f-a55db399d34f">StringCchCopy</a>



<a href="https://msdn.microsoft.com/0965b0f6-9588-4944-98d8-3aca3a3029fc">StringCchCopyEx</a>



<a href="https://msdn.microsoft.com/5803c6fa-d1ae-4c3b-8627-162039e8c31f">StringCchCopyN</a>



<a href="https://msdn.microsoft.com/228ddd78-9747-4a9a-b936-abfba6ff2940">StringCchCopyNEx</a>



<b>StringCchLength</b>
 

 

