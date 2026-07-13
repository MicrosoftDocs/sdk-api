---
UID: NF:winbase.GetCommTimeouts
title: GetCommTimeouts function (winbase.h)
description: Retrieves the time-out parameters for all read and write operations on a specified communications device.
helpviewer_keywords: ["GetCommTimeouts","GetCommTimeouts function","_win32_getcommtimeouts","base.getcommtimeouts","winbase/GetCommTimeouts"]
old-location: base\getcommtimeouts.htm
tech.root: base
ms.assetid: a5375b2e-0992-4e47-a20f-8a793addeef6
ms.date: 12/05/2018
ms.keywords: GetCommTimeouts, GetCommTimeouts function, _win32_getcommtimeouts, base.getcommtimeouts, winbase/GetCommTimeouts
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - GetCommTimeouts
 - winbase/GetCommTimeouts
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-comm-l1-1-2.dll
 - api-ms-win-core-comm-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCommTimeouts
---

# GetCommTimeouts function


## -description

Retrieves the time-out parameters for all read and write operations on a specified communications device.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param lpCommTimeouts [out]

A pointer to a 
<a href="/windows/desktop/api/winbase/ns-winbase-commtimeouts">COMMTIMEOUTS</a> structure in which the time-out information is returned.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more information about time-out values for communications devices, see the 
<a href="/windows/desktop/api/winbase/nf-winbase-setcommtimeouts">SetCommTimeouts</a> function.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-commtimeouts">COMMTIMEOUTS</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommtimeouts">SetCommTimeouts</a>