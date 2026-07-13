---
UID: NF:errhandlingapi.RemoveVectoredExceptionHandler
title: RemoveVectoredExceptionHandler function (errhandlingapi.h)
description: Unregisters a vectored exception handler.
helpviewer_keywords: ["RemoveVectoredExceptionHandler","RemoveVectoredExceptionHandler function","_win32_removevectoredexceptionhandler","base.removevectoredexceptionhandler","errhandlingapi/RemoveVectoredExceptionHandler"]
old-location: base\removevectoredexceptionhandler.htm
tech.root: Debug
ms.assetid: 94d54b75-e992-477f-ad4f-9b8a3bb44ffb
ms.date: 12/05/2018
ms.keywords: RemoveVectoredExceptionHandler, RemoveVectoredExceptionHandler function, _win32_removevectoredexceptionhandler, base.removevectoredexceptionhandler, errhandlingapi/RemoveVectoredExceptionHandler
req.header: errhandlingapi.h
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
 - RemoveVectoredExceptionHandler
 - errhandlingapi/RemoveVectoredExceptionHandler
dev_langs:
 - c++
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
 - RemoveVectoredExceptionHandler
---

## -description

Unregisters a vectored exception handler.

## -parameters

### -param Handle

A handle to the vectored exception handler previously registered using the [AddVectoredExceptionHandler function](nf-errhandlingapi-addvectoredexceptionhandler.md).

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more information, see [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers).

### Examples

For an example, see [Using a Vectored Exception Handler](/windows/desktop/Debug/using-a-vectored-exception-handler).

## -see-also

[AddVectoredExceptionHandler function](nf-errhandlingapi-addvectoredexceptionhandler.md), [Vectored Exception Handling](/windows/desktop/Debug/vectored-exception-handling)
