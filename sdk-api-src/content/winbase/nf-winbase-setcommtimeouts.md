---
UID: NF:winbase.SetCommTimeouts
title: SetCommTimeouts function (winbase.h)
description: Sets the time-out parameters for all read and write operations on a specified communications device.
helpviewer_keywords: ["SetCommTimeouts","SetCommTimeouts function","_win32_setcommtimeouts","base.setcommtimeouts","winbase/SetCommTimeouts"]
old-location: base\setcommtimeouts.htm
tech.root: base
ms.assetid: 71aa6ab3-d56c-43bc-9932-5b4e61fc4b30
ms.date: 12/05/2018
ms.keywords: SetCommTimeouts, SetCommTimeouts function, _win32_setcommtimeouts, base.setcommtimeouts, winbase/SetCommTimeouts
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
 - SetCommTimeouts
 - winbase/SetCommTimeouts
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
 - SetCommTimeouts
---

# SetCommTimeouts function


## -description

Sets the time-out parameters for all read and write operations on a specified communications device.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param lpCommTimeouts [in]

A pointer to a 
<a href="/windows/desktop/api/winbase/ns-winbase-commtimeouts">COMMTIMEOUTS</a> structure that contains the new time-out values.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-commtimeouts">COMMTIMEOUTS</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcommtimeouts">GetCommTimeouts</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>