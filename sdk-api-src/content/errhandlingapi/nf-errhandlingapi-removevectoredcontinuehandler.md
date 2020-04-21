---
UID: NF:errhandlingapi.RemoveVectoredContinueHandler
title: RemoveVectoredContinueHandler function (errhandlingapi.h)
description: Unregisters a vectored continue handler.helpviewer_keywords: ["RemoveVectoredContinueHandler","RemoveVectoredContinueHandler function","base.removevectoredcontinuehandler","errhandlingapi/RemoveVectoredContinueHandler"]
old-location: base\removevectoredcontinuehandler.htm
tech.root: Debug
ms.assetid: aed0bb01-a0f3-49c8-9d4a-ab8ddc09fc17
ms.date: 12/05/2018
ms.keywords: RemoveVectoredContinueHandler, RemoveVectoredContinueHandler function, base.removevectoredcontinuehandler, errhandlingapi/RemoveVectoredContinueHandler
f1_keywords:
- errhandlingapi/RemoveVectoredContinueHandler
dev_langs:
- c++
req.header: errhandlingapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-errorhandling-l1-1-1.dll
- KernelBase.dll
- API-MS-Win-Core-errorhandling-l1-1-2.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
- API-MS-Win-Core-ErrorHandling-L1-1-3.dll
api_name:
- RemoveVectoredContinueHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RemoveVectoredContinueHandler function


## -description


Unregisters a vectored continue handler.


## -parameters




### -param Handle

TBD




#### - Handler [in]

A pointer to a vectored exception handler previously registered using the 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler">AddVectoredContinueHandler</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler">AddVectoredContinueHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/Debug/vectored-exception-handling">Vectored Exception Handling</a>
 

 

