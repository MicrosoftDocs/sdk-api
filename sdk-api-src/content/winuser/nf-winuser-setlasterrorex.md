---
UID: NF:winuser.SetLastErrorEx
title: SetLastErrorEx function (winuser.h)
description: Sets the last-error code.
helpviewer_keywords: ["SetLastErrorEx","SetLastErrorEx function","_win32_setlasterrorex","base.setlasterrorex","winuser/SetLastErrorEx"]
old-location: base\setlasterrorex.htm
tech.root: Debug
ms.assetid: d97494db-868a-49d4-a613-e8beba86d4e6
ms.date: 12/05/2018
ms.keywords: SetLastErrorEx, SetLastErrorEx function, _win32_setlasterrorex, base.setlasterrorex, winuser/SetLastErrorEx
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetLastErrorEx
 - winuser/SetLastErrorEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetLastErrorEx
---

# SetLastErrorEx function


## -description

Sets the last-error code.

Currently, this function is identical to the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> function. The second parameter is ignored.

## -parameters

### -param dwErrCode [in]

The last-error code for the thread.

### -param dwType [in]

This parameter is ignored.

## -remarks

The last-error code is kept in thread local storage so that multiple threads do not overwrite each other's values.

Most functions call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> or <b>SetLastErrorEx</b> only when they fail. However, some system functions call 
<b>SetLastError</b> or <b>SetLastErrorEx</b> under conditions of success; those cases are noted in each function's documentation.

Applications can optionally retrieve the value set by this function by using the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function immediately after a function fails.

Error codes are 32-bit values (bit 31 is the most significant bit). Bit 29 is reserved for application-defined error codes; no system error code has this bit set. If you are defining an error code for your application, set this bit to indicate that the error code has been defined by the application and to ensure that your error code does not conflict with any system-defined error codes.

## -see-also

<a href="/windows/desktop/Debug/error-handling-functions">Error Handling Functions</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/Debug/last-error-code">Last-Error Code</a>