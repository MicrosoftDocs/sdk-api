---
UID: NF:winuser.ShutdownBlockReasonDestroy
title: ShutdownBlockReasonDestroy function (winuser.h)
description: Indicates that the system can be shut down and frees the reason string.
helpviewer_keywords: ["ShutdownBlockReasonDestroy","ShutdownBlockReasonDestroy function","base.shutdownblockreasondestroy","winuser/ShutdownBlockReasonDestroy"]
old-location: base\shutdownblockreasondestroy.htm
tech.root: base
ms.assetid: b7bf376a-79b5-4f63-b3ca-0d515c23d67c
ms.date: 12/05/2018
ms.keywords: ShutdownBlockReasonDestroy, ShutdownBlockReasonDestroy function, base.shutdownblockreasondestroy, winuser/ShutdownBlockReasonDestroy
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
 - ShutdownBlockReasonDestroy
 - winuser/ShutdownBlockReasonDestroy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - ShutdownBlockReasonDestroy
req.apiset: ext-ms-win-ntuser-misc-l1-1-0 (introduced in Windows 8)
---

# ShutdownBlockReasonDestroy function


## -description

Indicates that the system can be shut down and frees the reason string.

## -parameters

### -param hWnd [in]

A handle to the main window of the application.

## -returns

If the call succeeds, the return value is nonzero.

If the call fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function can only be called from the thread that created the window specified by the <i>hWnd</i> parameter. Otherwise, the function fails and the last error code is ERROR_ACCESS_DENIED.

If system shutdown has been previously blocked by the <a href="/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate">ShutdownBlockReasonCreate</a> function, this function frees the reason string. Otherwise, this function is a no-op.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate">ShutdownBlockReasonCreate</a>



<a href="/windows/desktop/Shutdown/shutting-down">Shutting Down</a>
