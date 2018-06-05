---
UID: NF:winddi.EngAcquireSemaphore
title: EngAcquireSemaphore function
author: windows-sdk-content
description: The EngAcquireSemaphore function acquires the resource associated with the semaphore for exclusive access by the calling thread.
old-location: display\engacquiresemaphore.htm
old-project: display
ms.assetid: da13ff30-7817-4ed4-9791-2d205a260259
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngAcquireSemaphore, EngAcquireSemaphore function [Display Devices], display.engacquiresemaphore, gdifncs_eae93ab5-f0f0-4d4e-a857-50ec8698527b.xml, winddi/EngAcquireSemaphore
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32.dll
-	GDI32Full.dll
api_name:
-	EngAcquireSemaphore
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngAcquireSemaphore function


## -description


The <b>EngAcquireSemaphore</b> function acquires the resource associated with the semaphore for exclusive access by the calling thread.


## -parameters




### -param hsem [in]

Handle to the semaphore associated with the resource to be acquired.


## -returns



None




## -remarks



<b>EngAcquireSemaphore</b> allows exclusive access to the driver resource associated with the semaphore by locking out all other threads from accessing the semaphore's resource.

A call to this routine should be followed with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a> as quickly as possible.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564760">EngCreateSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564819">EngDeleteSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564960">EngIsSemaphoreOwned</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564961">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a>
 

 

