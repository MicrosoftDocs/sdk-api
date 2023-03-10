---
UID: NF:winbase.DeleteFiber
title: DeleteFiber function (winbase.h)
description: Deletes an existing fiber.
helpviewer_keywords: ["DeleteFiber","DeleteFiber function","_win32_deletefiber","base.deletefiber","winbase/DeleteFiber"]
old-location: base\deletefiber.htm
tech.root: backup
ms.assetid: e1a7453a-6878-49dd-831f-1857a489e97f
ms.date: 12/05/2018
ms.keywords: DeleteFiber, DeleteFiber function, _win32_deletefiber, base.deletefiber, winbase/DeleteFiber
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
 - DeleteFiber
 - winbase/DeleteFiber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-fibers-l2-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-fibers-l2-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - KernelBase.dll
api_name:
 - DeleteFiber
---

# DeleteFiber function


## -description

Deletes an existing fiber.

## -parameters

### -param lpFiber [in]

The address of the fiber to be deleted.

## -remarks

The 
<b>DeleteFiber</b> function deletes all data associated with the fiber. This data includes the stack, a subset of the registers, and the fiber data.

If the currently running fiber calls 
<b>DeleteFiber</b>, its thread calls 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> and terminates. However, if a currently running fiber is deleted by another fiber, the thread running the deleted fiber is likely to terminate abnormally because the fiber stack has been freed.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-fibers">Using Fibers</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>