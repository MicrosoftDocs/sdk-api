---
UID: NF:winbase.QueryFullProcessImageNameA
title: QueryFullProcessImageNameA function (winbase.h)
description: Retrieves the full name of the executable image for the specified process. (ANSI)
helpviewer_keywords: ["PROCESS_NAME_NATIVE", "QueryFullProcessImageNameA", "winbase/QueryFullProcessImageNameA"]
old-location: base\queryfullprocessimagename.htm
tech.root: backup
ms.assetid: 49a9d1aa-30f3-45ea-a4ec-9f55df692b8b
ms.date: 12/05/2018
ms.keywords: PROCESS_NAME_NATIVE, QueryFullProcessImageName, QueryFullProcessImageName function, QueryFullProcessImageNameA, QueryFullProcessImageNameW, base.queryfullprocessimagename, winbase/QueryFullProcessImageName, winbase/QueryFullProcessImageNameA, winbase/QueryFullProcessImageNameW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryFullProcessImageNameW (Unicode) and QueryFullProcessImageNameA (ANSI)
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
 - QueryFullProcessImageNameA
 - winbase/QueryFullProcessImageNameA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-psapi-ansi-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-psapi-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
 - QueryFullProcessImageName
 - QueryFullProcessImageNameA
 - QueryFullProcessImageNameW
---

# QueryFullProcessImageNameA function


## -description

Retrieves the full name of the executable image for the specified process.

## -parameters

### -param hProcess [in]

A handle to the process. This handle must be created with the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param dwFlags [in]

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The name should use the Win32 path format.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_NAME_NATIVE"></a><a id="process_name_native"></a><dl>
<dt><b>PROCESS_NAME_NATIVE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The name should use the native system path format.

</td>
</tr>
</table>

### -param lpExeName [out]

The path to the executable image. If the function succeeds, this string is null-terminated.

### -param lpdwSize [in, out]

On input, specifies the size of the <i>lpExeName</i> buffer, in characters. On success, receives the number of characters written to the buffer, not including the null-terminating character.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later.





> [!NOTE]
> The winbase.h header defines QueryFullProcessImageName as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa">GetModuleFileNameEx</a>



<a href="/windows/desktop/api/psapi/nf-psapi-getprocessimagefilenamea">GetProcessImageFileName</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
