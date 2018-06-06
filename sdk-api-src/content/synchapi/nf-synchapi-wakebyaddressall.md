---
UID: NF:synchapi.WakeByAddressAll
title: WakeByAddressAll function
author: windows-sdk-content
description: Wakes all threads that are waiting for the value of an address to change.
old-location: base\wakebyaddressall.htm
old-project: Sync
ms.assetid: 2d538cea-06cb-4973-8677-27ebcde0aa6f
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: WakeByAddressAll, WakeByAddressAll function, base.wakebyaddressall, synchapi/WakeByAddressAll
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ITEMPROP, *LPITEMPROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - MinKernelBase.dll
api_name:
 - WakeByAddressAll
product: Windows
targetos: Windows
req.lib: Synchronization.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# WakeByAddressAll function


## -description


Wakes all threads that are waiting for the value of an address to change.


## -parameters




### -param Address [in]

The address to signal. If any threads have previously called 
      <a href="https://msdn.microsoft.com/d40de436-f71e-47f6-a8c3-549c2699eb4c">WaitOnAddress</a> for this address, the system wakes all 
      of the waiting threads.


## -returns



This function does not return a value.




## -remarks



Windows Store apps developers may need to obtain synchronization.lib by installing the <a href="http://go.microsoft.com/fwlink/p/?LinkID=258383">Windows Software Development Kit (SDK) for Windows 8</a>.

Only threads within the same process can be woken.




## -see-also




<a href="https://msdn.microsoft.com/d40de436-f71e-47f6-a8c3-549c2699eb4c">WaitOnAddress</a>
 

 

