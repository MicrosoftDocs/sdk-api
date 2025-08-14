---
UID: NF:pdh.PdhExpandCounterPathW
title: PdhExpandCounterPathW function (pdh.h)
description: Examines the specified computer (or local computer if none is specified) for counters and instances of counters that match the wildcard strings in the counter path. (Unicode)
helpviewer_keywords: ["PdhExpandCounterPath", "PdhExpandCounterPath function [Perf]", "PdhExpandCounterPathW", "_win32_pdhexpandcounterpath", "base.pdhexpandcounterpath", "pdh/PdhExpandCounterPath", "pdh/PdhExpandCounterPathW", "perf.pdhexpandcounterpath"]
old-location: perf\pdhexpandcounterpath.htm
tech.root: perf
ms.assetid: d90954ab-ec2f-42fd-90b7-66f59f3d1115
ms.date: 12/05/2018
ms.keywords: PdhExpandCounterPath, PdhExpandCounterPath function [Perf], PdhExpandCounterPathA, PdhExpandCounterPathW, _win32_pdhexpandcounterpath, base.pdhexpandcounterpath, pdh/PdhExpandCounterPath, pdh/PdhExpandCounterPathA, pdh/PdhExpandCounterPathW, perf.pdhexpandcounterpath
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhExpandCounterPathW (Unicode) and PdhExpandCounterPathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PdhExpandCounterPathW
 - pdh/PdhExpandCounterPathW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-eventing-pdh-l1-1-3.dll
 - ext-ms-win-eventing-pdh-l1-1-2.dll
 - Pdh.dll
api_name:
 - PdhExpandCounterPath
 - PdhExpandCounterPathA
 - PdhExpandCounterPathW
---

# PdhExpandCounterPathW function


## -description

Examines the specified computer (or local computer if none is specified) for counters and instances of counters that match the wildcard strings in the counter path.
		
<div class="alert"><b>Note</b>  This function is superseded by the <a href="/windows/desktop/api/pdh/nf-pdh-pdhexpandwildcardpatha">PdhExpandWildCardPath</a> function.</div><div> </div>

## -parameters

### -param szWildCardPath [in]

<b>Null</b>-terminated string that contains the counter path to expand. The function searches the computer specified in the path for matches. If the path does not specify a computer, the function searches the local computer. The maximum length of a counter path is PDH_MAX_COUNTER_PATH.

### -param mszExpandedPathList [out]

Caller-allocated buffer that receives the list of expanded counter paths that match the wildcard specification in <i>szWildCardPath</i>. Each counter path in this list is terminated by a <b>null</b> character. The list is terminated with two <b>NULL</b> characters. Set to <b>NULL</b> if <i>pcchPathListLength</i> is zero.

### -param pcchPathListLength [in, out]

Size of the <i>mszExpandedPathList</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

<div class="alert"><b>Note</b>  You must add one to the required size on Windows XP.</div>
<div> </div>

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>mszExpandedPathList</i> buffer is too small to contain the list of paths. This return value is expected if <i>pcchPathListLength</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid. For example, on some releases you could receive this error if the specified size on input is greater than zero but less than the required size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MEMORY_ALLOCATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to support this function.

</td>
</tr>
</table>

## -remarks

You should call this function twice, the first time to get the required buffer size (set <i>mszExpandedPathList</i> to <b>NULL</b> and <i>pcchPathListLength</i> to 0), and the second time to get the data.

The general counter path format is as follows:

\\computer\object(parent/instance#index)\counter

The parent, instance, index, and counter components of the counter path may contain either a valid name or a wildcard character. The computer, parent, instance, and index components are not necessary for all counters.

The counter paths that you must use is determined by the counter itself. For example, the LogicalDisk object has an instance index, so you must provide the #index, or a wildcard. Therefore, you could use the following format:

\LogicalDisk(*/*#*)\*

In comparison, the Process object does not require an instance index. Therefore, you could use the following format:

\Process(*)\ID Process

The following is a list of the possible formats:

<ul>
<li>\\computer\object(parent/instance#index)\counter</li>
<li>\\computer\object(parent/instance)\counter</li>
<li>\\computer\object(instance#index)\counter</li>
<li>\\computer\object(instance)\counter</li>
<li>\\computer\object\counter</li>
<li>\object(parent/instance#index)\counter</li>
<li>\object(parent/instance)\counter</li>
<li>\object(instance#index)\counter</li>
<li>\object(instance)\counter</li>
<li>\object\counter</li>
</ul>
If a wildcard character is specified in the parent name, all instances of the specified object that match the specified instance and counter fields will be returned.

If a wildcard character is specified in the instance name, all instances of the specified object and parent object will be returned if all instance names corresponding to the specified index match the wildcard character.

If a wildcard character is specified in the counter name, all counters of the specified object are returned.

Partial counter path string matches (for example, "pro*") are not supported.


#### Examples

The following example demonstrates how to this function.


```cpp

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR WILDCARD_PATH = L"\\Processor(*)\\*";

void wmain(void)
{
    PDH_STATUS Status;
    PWSTR EndOfPaths;
    PWSTR Paths = NULL;
    DWORD BufferSize = 0;

    Status = PdhExpandCounterPath(WILDCARD_PATH, Paths, &BufferSize);

    while (Status == PDH_MORE_DATA) 
    {
        Paths = (PWSTR)malloc(BufferSize * sizeof(WCHAR));
        Status = PdhExpandCounterPath(WILDCARD_PATH, Paths, &BufferSize);
    }

    if (Status != ERROR_SUCCESS) 
    {
        wprintf(L"\nPdhExpandCounterPath failed with status 0x%x", Status);
        goto Cleanup;
    }

    if (Paths == NULL) 
    {
        wprintf(L"\nThe counter path %s cannot be expanded.", WILDCARD_PATH);
        goto Cleanup;
    }

    EndOfPaths = Paths + BufferSize;

    // On Vista and later operating systems, the buffer is terminated with two 
    // null-terminator characters; however, on earlier systems, the buffer is
    // not terminated with two null-terminator characters. This covers both cases.
    for (PWSTR p = Paths; ((p != EndOfPaths) && (*p != L'\0')); p += wcslen(p) + 1) 
    {
        wprintf(L"\n%s", p);
    }

Cleanup:
    if (Paths) 
    {
        free(Paths);
    }
}

```






> [!NOTE]
> The pdh.h header defines PdhExpandCounterPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhexpandwildcardpatha">PdhExpandWildCardPath</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhmakecounterpatha">PdhMakeCounterPath</a>
