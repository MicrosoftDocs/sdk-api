---
UID: NF:errhandlingapi.FatalAppExitW
title: FatalAppExitW function (errhandlingapi.h)
description: Displays a message box and terminates the application when the message box is closed.helpviewer_keywords: ["FatalAppExit","FatalAppExit function","FatalAppExitA","FatalAppExitW","_win32_fatalappexit","base.fatalappexit","errhandlingapi/FatalAppExit","errhandlingapi/FatalAppExitA","errhandlingapi/FatalAppExitW"]
old-location: base\fatalappexit.htm
tech.root: Debug
ms.assetid: f18d8b16-ffe1-49f1-98be-ba8d49db86ef
ms.date: 12/05/2018
ms.keywords: FatalAppExit, FatalAppExit function, FatalAppExitA, FatalAppExitW, _win32_fatalappexit, base.fatalappexit, errhandlingapi/FatalAppExit, errhandlingapi/FatalAppExitA, errhandlingapi/FatalAppExitW
f1_keywords:
- errhandlingapi/FatalAppExit
dev_langs:
- c++
req.header: errhandlingapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FatalAppExitW (Unicode) and FatalAppExitA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
- API-MS-Win-Core-misc-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-ErrorHandling-L1-1-3.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
- FatalAppExit
- FatalAppExitA
- FatalAppExitW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FatalAppExitW function


## -description


Displays a message box and terminates the application when the message box is closed. If the system is running with a debug version of Kernel32.dll, the message box gives the user the opportunity to terminate the application or to cancel the message box and return to the application that called 
<b>FatalAppExit</b>.


## -parameters




### -param uAction [in]

This parameter must be zero.


### -param lpMessageText [in]

The null-terminated string that is displayed in the message box.


## -remarks



An application calls 
<b>FatalAppExit</b> only when it is not capable of terminating any other way. 





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/error-handling-functions">Error Handling Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-fatalexit">FatalExit</a>
 

 

