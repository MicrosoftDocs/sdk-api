---
UID: NF:errhandlingapi.SetLastError
title: SetLastError function (errhandlingapi.h)
description: Sets the last-error code for the calling thread.
helpviewer_keywords: ["SetLastError","SetLastError function","_win32_setlasterror","base.setlasterror","errhandlingapi/SetLastError"]
old-location: base\setlasterror.htm
tech.root: Debug
ms.assetid: d9da833f-36ca-4046-8d2f-cd4449dd3c63
ms.date: 12/05/2018
ms.keywords: SetLastError, SetLastError function, _win32_setlasterror, base.setlasterror, errhandlingapi/SetLastError
req.header: errhandlingapi.h
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
 - SetLastError
 - errhandlingapi/SetLastError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-errorhandling-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-errorhandling-l1-1-1.dll
 - API-MS-Win-Core-errorhandling-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ErrorHandling-L1-1-3.dll
 - vertdll.dll
api_name:
 - SetLastError
---

# SetLastError function


## -description

Sets the last-error code for the calling thread.

## -parameters

### -param dwErrCode [in]

The last-error code for the thread.

## -remarks

The last-error code is kept in thread local storage so that multiple threads do not overwrite each other's values.

Most functions call 
<b>SetLastError</b> or <a href="/windows/desktop/api/winuser/nf-winuser-setlasterrorex">SetLastErrorEx</a> only when they fail. However, some system functions call 
<b>SetLastError</b> or <b>SetLastErrorEx</b> under conditions of success; those cases are noted in each function's documentation.

Applications can optionally retrieve the value set by this function by using the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function immediately after a function fails.

Error codes are 32-bit values (bit 31 is the most significant bit). Bit 29 is reserved for application-defined error codes; no system error code has this bit set. If you are defining an error code for your application, set this bit to indicate that the error code has been defined by your application and to ensure that your error code does not conflict with any system-defined error codes.

## -see-also

<a href="/windows/desktop/Debug/error-handling-functions">Error Handling Functions</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/Debug/last-error-code">Last-Error Code</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setlasterrorex">SetLastErrorEx</a>