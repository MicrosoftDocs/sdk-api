---
UID: NF:winuser.ShutdownBlockReasonCreate
title: ShutdownBlockReasonCreate function (winuser.h)
description: Indicates that the system cannot be shut down and sets a reason string to be displayed to the user if system shutdown is initiated.
helpviewer_keywords: ["ShutdownBlockReasonCreate","ShutdownBlockReasonCreate function","base.shutdownblockreasoncreate","winuser/ShutdownBlockReasonCreate"]
old-location: base\shutdownblockreasoncreate.htm
tech.root: base
ms.assetid: 4c6f9159-fac2-431e-bbdf-c35c4cdb25ac
ms.date: 12/05/2018
ms.keywords: ShutdownBlockReasonCreate, ShutdownBlockReasonCreate function, base.shutdownblockreasoncreate, winuser/ShutdownBlockReasonCreate
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
 - ShutdownBlockReasonCreate
 - winuser/ShutdownBlockReasonCreate
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
 - ShutdownBlockReasonCreate
req.apiset: ext-ms-win-ntuser-misc-l1-1-0 (introduced in Windows 8)
---

# ShutdownBlockReasonCreate function


## -description

Indicates that the system cannot be shut down and sets a reason string to be displayed to the user if system shutdown is initiated.

## -parameters

### -param hWnd [in]

A handle to the main window of the application.

### -param pwszReason [in]

The reason the application must block system shutdown. This string will be truncated for display purposes after MAX_STR_BLOCKREASON characters.

## -returns

If the call succeeds, the return value is nonzero.

If the call fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function can only be called from the thread that created the window specified by the <i>hWnd</i> parameter. Otherwise, the function fails and the last error code is ERROR_ACCESS_DENIED.

Applications should call this function as they begin an operation that cannot be interrupted, such as burning a CD or DVD. When the operation has completed, call the <a href="/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy">ShutdownBlockReasonDestroy</a> function to indicate that the system can be shut down.

Because users are typically in a hurry when shutting down the system, they may spend only  a few seconds looking at the shutdown reasons that are displayed by the system. Therefore, it is important that your reason strings are short and clear. For example "A CD burn is in progress." is better than "This application is blocking system shutdown because a CD burn is in progress. Do not shut down."

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy">ShutdownBlockReasonDestroy</a>



<a href="/windows/desktop/Shutdown/shutting-down">Shutting Down</a>
