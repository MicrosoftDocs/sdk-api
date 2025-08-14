---
UID: NF:memoryapi.RegisterBadMemoryNotification
title: RegisterBadMemoryNotification function (memoryapi.h)
description: Registers a bad memory notification that is called when one or more bad memory pages are detected.
helpviewer_keywords: ["RegisterBadMemoryNotification","RegisterBadMemoryNotification function","base.registerbadmemorynotification","winbase/RegisterBadMemoryNotification"]
old-location: base\registerbadmemorynotification.htm
tech.root: base
ms.assetid: 4a3a621a-49ed-4538-9e36-b8eab5d57eb7
ms.date: 12/05/2018
ms.keywords: RegisterBadMemoryNotification, RegisterBadMemoryNotification function, base.registerbadmemorynotification, winbase/RegisterBadMemoryNotification
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
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterBadMemoryNotification
 - memoryapi/RegisterBadMemoryNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - RegisterBadMemoryNotification
---

# RegisterBadMemoryNotification function


## -description

Registers a bad memory notification that is called when one or more bad memory pages are detected and the system 
    cannot remove at least one of them (for example if the pages contains modified data that has not yet been written 
    to the pagefile.)

## -parameters

### -param Callback [in]

A pointer to the application-defined 
      <a href="/previous-versions/windows/desktop/legacy/hh691011(v=vs.85)">BadMemoryCallbackRoutine</a> function to 
      register.

## -returns

Registration handle that represents the callback notification. Can be passed to the 
      <a href="/windows/desktop/api/memoryapi/nf-memoryapi-unregisterbadmemorynotification">UnregisterBadMemoryNotification</a> 
      function when no longer needed.

## -remarks

To compile an application that calls this function, define <b>_WIN32_WINNT</b> as 
    <b>_WIN32_WINNT_WIN8</b> or higher. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.