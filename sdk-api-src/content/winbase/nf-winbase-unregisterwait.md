---
UID: NF:winbase.UnregisterWait
title: UnregisterWait function (winbase.h)
description: Cancels a registered wait operation issued by the RegisterWaitForSingleObject function. (UnregisterWait)
helpviewer_keywords: ["UnregisterWait","UnregisterWait function","_win32_unregisterwait","base.unregisterwait","winbase/UnregisterWait"]
old-location: base\unregisterwait.htm
tech.root: backup
ms.assetid: 9ae8879f-0dbd-4d04-ae6e-094324f82acf
ms.date: 12/05/2018
ms.keywords: UnregisterWait, UnregisterWait function, _win32_unregisterwait, base.unregisterwait, winbase/UnregisterWait
req.header: winbase.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnregisterWait
 - winbase/UnregisterWait
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - UnregisterWait
---

# UnregisterWait function


## -description

Cancels a registered wait operation issued by the 
<a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a> function.

To use a completion event, call the 
<a href="/windows/desktop/Sync/unregisterwaitex">UnregisterWaitEx</a> function.

## -parameters

### -param WaitHandle [in]

The wait handle. This handle is returned by the 
<a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If any callback functions associated with the timer have not completed when <b>UnregisterWait</b> is called, <b>UnregisterWait</b> unregisters the wait on the callback functions and fails with the <b>ERROR_IO_PENDING</b> error code. The error code does not indicate that the function has failed, and the function does not need to be called again. If your code requires an error code to set only when the unregister operation has failed, call <a href="/windows/desktop/Sync/unregisterwaitex">UnregisterWaitEx</a> instead.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/ProcThread/thread-pooling">Thread Pooling</a>



<a href="/windows/desktop/Sync/unregisterwaitex">UnregisterWaitEx</a>
