---
UID: NF:winbase.lstrcmpA
title: lstrcmpA function
author: windows-sdk-content
description: Compares two character strings. The comparison is case-sensitive.
old-location: menurc\lstrcmp.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrcmp.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "_win32_lstrcmp, _win32_lstrcmp_cpp, lstrcmp, lstrcmp function [Menus and Other Resources], lstrcmpA, lstrcmpW, menurc.lstrcmp, winbase/lstrcmp, winbase/lstrcmpA, winbase/lstrcmpW, winui._win32_lstrcmp"
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
req.unicode-ansi: lstrcmpW (Unicode) and lstrcmpA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-String-Obsolete-l1-1-0.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-String-Obsolete-l1-1-1.dll
-	API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
-	API-MS-Win-Core-misc-l1-1-0.dll
-	KernelBase.dll
-	MinKernelBase.dll
api_name:
-	lstrcmp
-	lstrcmpA
-	lstrcmpW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# lstrcmpA function


## -description


Compares two character strings. The comparison is case-sensitive.

To perform a comparison that is not case-sensitive, use the <a href="https://msdn.microsoft.com/7edd4896-04d3-4b71-9ce6-d64149d683e0">lstrcmpi</a> function.


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

The function calls <a href="https://msdn.microsoft.com/264c67b6-848d-48ef-9bfa-4990bfa2fbf5">CompareStringEx</a>, using the current thread locale, and subtracts 2 from the result, to maintain the C run-time conventions for comparing strings. 

The language (user locale) selected by the user at setup time, or through Control Panel, determines which string is greater (or whether the strings are the same). If no language (user locale) is selected, the system performs the comparison by using default values.

With a double-byte character set (DBCS) version of the system, this function can compare two DBCS strings. 

The <b>lstrcmp</b> function uses a word sort, rather than a string sort. A word sort treats hyphens and apostrophes differently than it treats other symbols that are not alphanumeric, in order to ensure that words such as "coop" and "co-op" stay together within a sorted list. For a detailed discussion of word sorts and string sorts, see <a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>. 

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
See <a href="https://msdn.microsoft.com/4034f479-ad29-4c6f-82c6-977f420c4d4d">Security Considerations: International Features</a> for security considerations regarding 

choice of comparison functions.




## -see-also




<a href="winui._win32_CompareString">CompareString</a>



<a href="winui._win32_CompareStringEx">CompareStringEx</a>



<a href="https://msdn.microsoft.com/6a457076-7992-4912-8ac5-2258f9651a8c">CompareStringOrdinal</a>



<b>Conceptual</b>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>



<a href="https://msdn.microsoft.com/346f6c95-6ebe-4e73-8f29-2778cc813e36">lstrcat</a>



<a href="https://msdn.microsoft.com/7edd4896-04d3-4b71-9ce6-d64149d683e0">lstrcmpi</a>



<a href="https://msdn.microsoft.com/3960fe0e-954d-4463-bc81-e1682e468278">lstrcpy</a>



<a href="https://msdn.microsoft.com/0024853f-3a1f-4742-bc5e-f0ca89e23f3a">lstrlen</a>
 

 

