---
UID: NF:winuser.GetWindowWord
tech.root: winmsg
title: GetWindowWord
ms.date: 02/23/2023
targetos: Windows
description: Retrieves the 16-bit (**DWORD**) value at the specified offset into the extra window memor
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winuser.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: User32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - user32.dll
api_name:
 - GetWindowWord
f1_keywords:
 - GetWindowWord
 - winuser/GetWindowWord
dev_langs:
 - c++
helpviewer_keywords:
 - GetWindowWord
---

## -description

Retrieves the 16-bit (**DWORD**) value at the specified offset into the extra window memory. 

## -parameters

### -param hWnd

A handle to the window and, indirectly, the class to which the window belongs.

### -param nIndex

The zero-based offset to the value to be retrieved. Valid values are in the range zero through the number of bytes of extra window memory, minus four; for example, if you specified 12 or more bytes of extra memory, a value of 8 would be an index to the third 32-bit integer. To retrieve any other value, specify one of the following values.


| Constant | Value | Meaning |
|-----------|-------|---------|
| GWW_HINSTANCE | -6 | Retrieves a handle to the application instance. |
| GWW_HWNDPARENT -8 | Retrieves a handle to the parent window, if any. |
| GWW_ID | -12 | Retrieves the identifier of the window. |



## -returns

If the function succeeds, the return value is the requested value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

## -remarks

Reserve extra window memory by specifying a nonzero value in the <b>cbWndExtra</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a> structure used with the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. 

## -see-also

