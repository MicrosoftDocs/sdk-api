---
UID: NF:winuser.ShutdownBlockReasonQuery
title: ShutdownBlockReasonQuery function (winuser.h)
description: Retrieves the reason string set by the ShutdownBlockReasonCreate function.
helpviewer_keywords: ["ShutdownBlockReasonQuery","ShutdownBlockReasonQuery function","base.shutdownblockreasonquery","winuser/ShutdownBlockReasonQuery"]
old-location: base\shutdownblockreasonquery.htm
tech.root: base
ms.assetid: 8c92ebbb-1692-4c14-b32a-17f59b8ab7a3
ms.date: 12/05/2018
ms.keywords: ShutdownBlockReasonQuery, ShutdownBlockReasonQuery function, base.shutdownblockreasonquery, winuser/ShutdownBlockReasonQuery
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - ShutdownBlockReasonQuery
 - winuser/ShutdownBlockReasonQuery
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
 - ShutdownBlockReasonQuery
---

# ShutdownBlockReasonQuery function


## -description

Retrieves the reason string set by the <a href="/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate">ShutdownBlockReasonCreate</a> function.

## -parameters

### -param hWnd [in]

A handle to the main window of the application.

### -param pwszBuff [out, optional]

A pointer to a buffer that receives the reason string. If this parameter is <b>NULL</b>, the function retrieves the number of characters in the reason string.

### -param pcchBuff [in, out]

A pointer to a variable that specifies the size of the <i>pwszBuff</i> buffer, in characters. If the function succeeds, this variable receives the number of characters copied into the buffer, including the <b>null</b>-terminating character. If the buffer is too small, the variable receives the required buffer size, in characters, not including the <b>null</b>-terminating character.

## -returns

If the call succeeds, the return value is nonzero.

If the call fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function can only be called from the thread that created the window specified by the <i>hWnd</i> parameter. Otherwise, the function fails and the last error code is ERROR_ACCESS_DENIED.


#### Examples

The following example retrieves the required buffer size, allocates memory for the reason string, retrieves the reason string, and displays the string as debug output.


```cpp
#include <windows.h>

#pragma comment(lib, "User32.lib")

HWND hWnd;

BOOL DisplayShutdownBlockReason()
{
    DWORD cch=0;

    if (ShutdownBlockReasonQuery(hWnd, NULL, &cch)) 
    { 
        WCHAR *pch = (WCHAR *)LocalAlloc(LMEM_FIXED, cch * sizeof(*pch)); 
        if (NULL != pch) 
        { 
            if (ShutdownBlockReasonQuery(hWnd, pch, &cch)) 
            { 
                OutputDebugStringW(L"Shutdown block reason: "); 
                OutputDebugStringW(pch); 
                OutputDebugStringW(L"\n"); 
            } 
            LocalFree(pch); 
            return TRUE;
        } 
    }
    return FALSE;
}

```

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate">ShutdownBlockReasonCreate</a>



<a href="/windows/desktop/Shutdown/shutting-down">Shutting Down</a>