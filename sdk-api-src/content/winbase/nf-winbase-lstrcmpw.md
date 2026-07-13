---
UID: NF:winbase.lstrcmpW
title: lstrcmpW function (winbase.h)
description: Compares two character strings. The comparison is case-sensitive. (Unicode)
helpviewer_keywords: ["_win32_lstrcmp", "_win32_lstrcmp_cpp", "lstrcmp", "lstrcmp function [Menus and Other Resources]", "lstrcmpW", "menurc.lstrcmp", "winbase/lstrcmp", "winbase/lstrcmpW", "winui._win32_lstrcmp"]
old-location: menurc\lstrcmp.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrcmp.htm
ms.date: 12/05/2018
ms.keywords: _win32_lstrcmp, _win32_lstrcmp_cpp, lstrcmp, lstrcmp function [Menus and Other Resources], lstrcmpA, lstrcmpW, menurc.lstrcmp, winbase/lstrcmp, winbase/lstrcmpA, winbase/lstrcmpW, winui._win32_lstrcmp
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lstrcmpW (Unicode) and lstrcmpA (ANSI)
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
 - lstrcmpW
 - winbase/lstrcmpW
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
 - lstrcmp
 - lstrcmpA
 - lstrcmpW
---

# lstrcmpW function


## -description

Compares two character strings. The comparison is case-sensitive.

To perform a comparison that is not case-sensitive, use the <a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpia">lstrcmpi</a> function.

## -parameters

### -param lpString1 [in]

Type: <b>LPCTSTR</b>

The first null-terminated string to be compared.

### -param lpString2 [in]

Type: <b>LPCTSTR</b>

The second null-terminated string to be compared.

## -returns

Type: <b>int</b>

If the string pointed to by 
						<i>lpString1</i> is less than the string pointed to by 
						<i>lpString2</i>, the return value is negative. If the string pointed to by 
						<i>lpString1</i> is greater than the string pointed to by 
						<i>lpString2</i>, the return value is positive. If the strings are equal, the return value is zero.

## -remarks

The <b>lstrcmp</b> function compares two strings by checking the first characters against each other, the second characters against each other, and so on until it finds an inequality or reaches the ends of the strings. 

 Note that the <i>lpString1</i> and <i>lpString2</i> parameters must be null-terminated, otherwise the string comparison can be incorrect. 

The function calls <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a>, using the current thread locale, and subtracts 2 from the result, to maintain the C run-time conventions for comparing strings. 

The language (user locale) selected by the user at setup time, or through Control Panel, determines which string is greater (or whether the strings are the same). If no language (user locale) is selected, the system performs the comparison by using default values.

With a double-byte character set (DBCS) version of the system, this function can compare two DBCS strings. 

The <b>lstrcmp</b> function uses a word sort, rather than a string sort. A word sort treats hyphens and apostrophes differently than it treats other symbols that are not alphanumeric, in order to ensure that words such as "coop" and "co-op" stay together within a sorted list. For a detailed discussion of word sorts and string sorts, see <a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>. 

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
See <a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a> for security considerations regarding choice of comparison functions.





> [!NOTE]
> The winbase.h header defines lstrcmp as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringordinal">CompareStringOrdinal</a>



<b>Conceptual</b>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/menurc/strings">Strings</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcata">lstrcat</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpia">lstrcmpi</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcpya">lstrcpy</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrlena">lstrlen</a>
