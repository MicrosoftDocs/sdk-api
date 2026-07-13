---
UID: NF:winbase.lstrcpyA
title: lstrcpyA function (winbase.h)
description: Copies a string to a buffer. (ANSI)
helpviewer_keywords: ["lstrcpyA", "winbase/lstrcpyA"]
old-location: menurc\lstrcpy.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrcpy.htm
ms.date: 12/05/2018
ms.keywords: _win32_lstrcpy, _win32_lstrcpy_cpp, lstrcpy, lstrcpy function [Menus and Other Resources], lstrcpyA, lstrcpyW, menurc.lstrcpy, winbase/lstrcpy, winbase/lstrcpyA, winbase/lstrcpyW, winui._win32_lstrcpy
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lstrcpyA
 - winbase/lstrcpyA
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
api_name:
 - lstrcpy
 - lstrcpyA
 - lstrcpyW
---

# lstrcpyA function


## -description

Copies a string to a buffer.
<div class="alert"><b>Warning</b>  Do not use. Consider using <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a> instead. See Remarks.</div><div> </div>

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

Consider using <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a> instead; use either 
				<code>StringCchCopy(buffer, sizeof(buffer)/sizeof(buffer[0]), src);</code>, 
				being aware that <code>buffer</code> must not be a pointer or 
				use <code>StringCchCopy(buffer, ARRAYSIZE(buffer), src);</code>, 
				being aware that, when copying to a pointer, the caller is responsible for 
				passing in the size of the pointed-to memory in characters. 





> [!NOTE]
> The winbase.h header defines lstrcpy as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopya">StringCbCopy</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyexa">StringCbCopyEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyna">StringCbCopyN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopynexa">StringCbCopyNEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyexa">StringCchCopyEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyna">StringCchCopyN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopynexa">StringCchCopyNEx</a>



<a href="/windows/desktop/menurc/strings">Strings</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpa">lstrcmp</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpia">lstrcmpi</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrlena">lstrlen</a>
