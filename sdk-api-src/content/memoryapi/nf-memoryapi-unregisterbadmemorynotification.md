---
UID: NF:memoryapi.UnregisterBadMemoryNotification
title: UnregisterBadMemoryNotification function (memoryapi.h)
author: windows-sdk-content
description: Closes the specified bad memory notification handle.
old-location: base\unregisterbadmemorynotification.htm
tech.root: Memory
ms.assetid: 8c1246fe-341a-4b21-922d-ec8a9c82a6df
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UnregisterBadMemoryNotification, UnregisterBadMemoryNotification function, base.unregisterbadmemorynotification, winbase/UnregisterBadMemoryNotification
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - API-MS-Win-Core-memory-l1-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - UnregisterBadMemoryNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UnregisterBadMemoryNotification function


## -description


Closes the specified bad memory notification handle.


## -parameters




### -param RegistrationHandle [in]

Registration handle returned from the 
      <a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-registerbadmemorynotification">RegisterBadMemoryNotification</a> 
      function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To compile an application that calls this function, define <b>_WIN32_WINNT</b> as 
    <b>_WIN32_WINNT_WIN8</b> or higher. For more information, see 
    <a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.



