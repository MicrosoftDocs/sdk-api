---
UID: NF:handleapi.CompareObjectHandles
title: CompareObjectHandles function (handleapi.h)
description: Compares two object handles to determine if they refer to the same underlying kernel object.
helpviewer_keywords: ["CompareObjectHandles","CompareObjectHandles function","base.compareobjecthandles","handleapi/CompareObjectHandles"]
old-location: base\compareobjecthandles.htm
tech.root: winprog
ms.assetid: 06F22A46-0999-4622-8D62-23465C92A997
ms.date: 12/05/2018
ms.keywords: CompareObjectHandles, CompareObjectHandles function, base.compareobjecthandles, handleapi/CompareObjectHandles
req.header: handleapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernelbase.lib
req.dll: Kernelbase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CompareObjectHandles
 - handleapi/CompareObjectHandles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernelbase.dll
 - api-ms-win-core-handle-l1-1-0.lib
 - api-ms-win-core-handle-l1-1-0.dll
 - Kernel32.dll
api_name:
 - CompareObjectHandles
---

# CompareObjectHandles function


## -description

Compares two object handles to determine if they refer to the same underlying kernel object.

## -parameters

### -param hFirstObjectHandle [in]

The first object handle to compare.

### -param hSecondObjectHandle [in]

The second object handle to compare.

## -returns

A Boolean value that indicates if the two handles refer to the same underlying kernel object. TRUE if the same, otherwise FALSE.

## -remarks

The <b>CompareObjectHandles</b> function is useful to determine if two kernel handles refer to the same kernel object without imposing a requirement that specific access rights be granted to either handle in order to perform the comparison.  For example, if a process desires to determine whether a process handle is a handle to the current process, a call to <b>CompareObjectHandles</b> (GetCurrentProcess (), hProcess) can be used to determine if hProcess refers to the current process.  Notably, this does not require the use of object-specific access rights, whereas in this example, calling <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid">GetProcessId</a> to check the process IDs of two process handles imposes a requirement that the handles grant PROCESS_QUERY_LIMITED_INFORMATION access. However it is legal for a process handle to not have that access right granted depending on how the handle is intended to be used.


#### Examples

The following code sample creates three handles, two of which refer to the same object, then compares them to show that identical underlying kernel objects will return TRUE, while non-identical objects will return FALSE.


``` syntax
#include <windows.h>
#include <stdio.h>
#include <wchar.h>

HANDLE Event1;
HANDLE Event2;
HANDLE Event3;

	// Create a handle to a named event.
Event1 = CreateEventW (NULL, TRUE, FALSE, L"{75A520B7-2C11-4809-B43A-0D31FB1FDD19}");
if (Event1 == NULL) {	ExitProcess (0);	}

	// Create a handle to the same event.
Event2 = CreateEventW (NULL, TRUE, FALSE, L"{75A520B7-2C11-4809-B43A-0D31FB1FDD19}");
if (Event2 == NULL) {	ExitProcess (0);	}

	// Create a handle to an anonymous, unnamed event.
Event3 = CreateEventW (NULL, TRUE, FALSE, NULL);
if (Event3 == NULL) {	ExitProcess (0);	}

	// Compare two handles to the same kernel object.
if (CompareObjectHandles (Event1, Event2) != FALSE) 
	{	// This message should be printed by the program.
		wprintf (L"Event1 and Event2 refer to the same underlying event object.\n");
	}

	// Compare two handles to different kernel objects.
if (CompareObjectHandles (Event1, Event3) == FALSE) 
	{	// This message should be printed by the program.
		wprintf (L"Event1 and Event3 refer to different underlying event objects.  (Error %lu)\n", GetLastError ());		
	}

	// Compare two handles to different kernel objects, each of a different type of kernel object.
	// The comparison is legal to make, though the function will always return FALSE and indicate 
	// a last error status of ERROR_NOT_SAME_OBJECT.
if (CompareObjectHandles (Event1, GetCurrentProcess ()) == FALSE) 
	{	// This message should be printed by the program.
		wprintf (L"Event1 and the current process refer to different underlying kernel objects.  (Error %lu)\n", GetLastError ());
	}

```


## -see-also

<a href="/windows/desktop/SysInfo/handle-and-object-functions">Handle and Object Functions</a>
