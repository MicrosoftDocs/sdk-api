---
UID: NF:winddi.EngInitializeSafeSemaphore
title: EngInitializeSafeSemaphore function
author: windows-sdk-content
description: The EngInitializeSafeSemaphore function initializes the specified safe semaphore.
old-location: display\enginitializesafesemaphore.htm
old-project: display
ms.assetid: 17b614b0-1c41-442c-b787-978eac3ade45
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: EngInitializeSafeSemaphore, EngInitializeSafeSemaphore function [Display Devices], display.enginitializesafesemaphore, gdifncs_92f07217-a6d2-4996-99a9-eb289a713e19.xml, winddi/EngInitializeSafeSemaphore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngInitializeSafeSemaphore
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngInitializeSafeSemaphore function


## -description


The <b>EngInitializeSafeSemaphore</b> function initializes the specified safe semaphore. 


## -parameters




### -param pssem [out]

Pointer to the driver-allocated <a href="https://msdn.microsoft.com/library/windows/hardware/ff565007">ENGSAFESEMAPHORE</a> structure to be initialized.


## -returns



<b>EngInitializeSafeSemaphore</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -remarks



<b>EngInitializeSafeSemaphore</b> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff564814">EngDeleteSafeSemaphore</a> are thread-safe, operating under a lock and maintaining a reference count on the semaphore. This guarantees that only one semaphore is created regardless of the number of simultaneous calls to it, and that the semaphore exists until the last reference to it is released.

Once the safe semaphore is initialized, the driver can call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a> with the <b>hsem</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565007">ENGSAFESEMAPHORE</a> structure for synchronization.

Callers of <b>EngInitializeSafeSemaphore</b> should call <b>EngDeleteSafeSemaphore</b> when they no longer need the semaphore.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565007">ENGSAFESEMAPHORE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564814">EngDeleteSafeSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564960">EngIsSemaphoreOwned</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564961">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a>
 

 

