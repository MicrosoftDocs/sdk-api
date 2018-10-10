---
UID: NF:winbase.UnregisterWait
title: UnregisterWait function
author: windows-sdk-content
description: Cancels a registered wait operation issued by the RegisterWaitForSingleObject function.
old-location: base\unregisterwait.htm
tech.root: Sync
ms.assetid: 9ae8879f-0dbd-4d04-ae6e-094324f82acf
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: UnregisterWait, UnregisterWait function, _win32_unregisterwait, base.unregisterwait, winbase/UnregisterWait
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - UnregisterWait
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnregisterWait function


## -description


Cancels a registered wait operation issued by the 
<a href="https://msdn.microsoft.com/d0cd8b28-6e20-449a-94dd-cca2be46b812">RegisterWaitForSingleObject</a> function.

To use a completion event, call the 
<a href="https://msdn.microsoft.com/ea700e55-fce7-46cd-bb96-0c129b429d46">UnregisterWaitEx</a> function.


## -parameters




### -param WaitHandle [in]

The wait handle. This handle is returned by the 
<a href="https://msdn.microsoft.com/d0cd8b28-6e20-449a-94dd-cca2be46b812">RegisterWaitForSingleObject</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If any callback functions associated with the timer have not completed when <b>UnregisterWait</b> is called, <b>UnregisterWait</b> unregisters the wait on the callback functions and fails with the <b>ERROR_IO_PENDING</b> error code. The error code does not indicate that the function has failed, and the function does not need to be called again. If your code requires an error code to set only when the unregister operation has failed, call <a href="https://msdn.microsoft.com/ea700e55-fce7-46cd-bb96-0c129b429d46">UnregisterWaitEx</a> instead.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/d0cd8b28-6e20-449a-94dd-cca2be46b812">RegisterWaitForSingleObject</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/a5e52080-35d4-47f5-9050-90889e3bf2f8">Thread Pooling</a>



<a href="https://msdn.microsoft.com/ea700e55-fce7-46cd-bb96-0c129b429d46">UnregisterWaitEx</a>
 

 

