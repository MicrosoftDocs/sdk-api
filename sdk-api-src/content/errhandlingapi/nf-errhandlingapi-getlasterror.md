---
UID: NF:errhandlingapi.GetLastError
title: GetLastError function (errhandlingapi.h)
description: Retrieves the calling thread's last-error code value.
helpviewer_keywords: ["GetLastError","GetLastError function","_win32_getlasterror","base.getlasterror","errhandlingapi/GetLastError"]
old-location: base\getlasterror.htm
tech.root: Debug
ms.assetid: d852e148-985c-416f-a5a7-27b6914b45d4
ms.date: 02/02/2024
ms.keywords: GetLastError, GetLastError function, _win32_getlasterror, base.getlasterror, errhandlingapi/GetLastError
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
 - GetLastError
 - errhandlingapi/GetLastError
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
 - GetLastError
---

# GetLastError function

## -description

Retrieves the calling thread's last-error code value. The last-error code is maintained on a per-thread basis. Multiple threads do not overwrite each other's last-error code.

<b>Visual Basic:</b> Applications should call <b>err.LastDllError</b> instead of <b>GetLastError</b>.

## -returns

The return value is the calling thread's last-error code.

The Return Value section of the documentation for each function that sets the last-error code notes the conditions under which the function sets the last-error code. Most functions that set the thread's last-error code set it when they fail. However, some functions also set the last-error code when they succeed. If the function is not documented to set the last-error code, the value returned by this function is simply the most recent last-error code to have been set; some functions set the last-error code to 0 on success and others do not.

## -remarks

Functions executed by the calling thread set this value by calling the [SetLastError](nf-errhandlingapi-setlasterror.md) function. You should call the <b>GetLastError</b> function immediately when a function's return value indicates that such a call will return useful data. That is because some functions call <b>SetLastError</b> with a zero when they succeed, wiping out the error code set by the most recently failed function.

To obtain an error string for system error codes, use the [FormatMessage](../winbase/nf-winbase-formatmessage.md) function. For a complete list of error codes provided by the operating system, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

The error codes returned by a function are not part of the Windows API specification and can vary by operating system or device driver. For this reason, we cannot provide the complete list of error codes that can be returned by each function. There are also many functions whose documentation does not include even a partial list of error codes that can be returned.

Error codes are 32-bit values (bit 31 is the most significant bit). Bit 29 is reserved for application-defined error codes; no system error code has this bit set. If you are defining an error code for your application, set this bit to one. That indicates that the error code has been defined by an application, and ensures that your error code does not conflict with any error codes defined by the system.

To convert a system error into an <b>HRESULT</b> value, use the <a href="/windows/win32/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro.

#### Examples

For an example, see <a href="/windows/win32/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>.

## -see-also

[Error Handling Functions](/windows/win32/Debug/error-handling-functions)

[FormatMessage](../winbase/nf-winbase-formatmessage.md)

[HRESULT_FROM_WIN32](../winerror/nf-winerror-hresult_from_win32.md)

[Last-Error Code](/windows/win32/Debug/last-error-code)

[SetLastError](nf-errhandlingapi-setlasterror.md)

[SetLastErrorEx](../winuser/nf-winuser-setlasterrorex.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
