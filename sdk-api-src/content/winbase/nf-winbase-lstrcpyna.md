---
UID: NF:winbase.lstrcpynA
title: lstrcpynA function (winbase.h)
description: Copies a specified number of characters from a source string into a buffer.Warning  Do not use. (ANSI)
helpviewer_keywords: ["lstrcpynA", "winbase/lstrcpynA"]
old-location: menurc\lstrcpyn.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrcpyn.htm
ms.date: 12/05/2018
ms.keywords: _win32_lstrcpyn, _win32_lstrcpyn_cpp, lstrcpyn, lstrcpyn function [Menus and Other Resources], lstrcpynA, lstrcpynW, menurc.lstrcpyn, winbase/lstrcpyn, winbase/lstrcpynA, winbase/lstrcpynW, winui._win32_lstrcpyn
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lstrcpynA
 - winbase/lstrcpynA
dev_langs:
 - c++
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
---

# lstrcpynA function


## -description

Copies a specified number of characters from a source string into a buffer.
<div class="alert"><b>Warning</b>  Do not use. Consider using <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a> instead. See Remarks.</div><div> </div>

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

Consider using <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a> instead; use either 
				<code>StringCchCopy(buffer, sizeof(buffer)/sizeof(buffer[0]), src);</code>, 
				being aware that <code>buffer</code> must not be a pointer or 
				use <code>StringCchCopy(buffer, ARRAYSIZE(buffer), src);</code>, 
				being aware that, when copying to a pointer, the caller is responsible for 
				passing in the size of the pointed-to memory in characters. 

Review <a href="/windows/desktop/AppUIStart/sec-ui">Security Considerations: Windows User Interface</a> before continuing.





> [!NOTE]
> The winbase.h header defines lstrcpyn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopya">StringCbCopy</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyexa">StringCbCopyEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyna">StringCbCopyN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopynexa">StringCbCopyNEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcblengtha">StringCbLength</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyexa">StringCchCopyEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyna">StringCchCopyN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopynexa">StringCchCopyNEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchlengtha">StringCchLength</a>



<a href="/windows/desktop/menurc/strings">Strings</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpa">lstrcmp</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpia">lstrcmpi</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrlena">lstrlen</a>
