---
UID: NF:winddi.EngCreateSemaphore
title: EngCreateSemaphore function
author: windows-driver-content
description: The EngCreateSemaphore function creates a semaphore object.
old-location: display\engcreatesemaphore.htm
old-project: display
ms.assetid: 02b68914-5007-4bfb-ac8a-0269447ab26b
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: EngCreateSemaphore, EngCreateSemaphore function [Display Devices], display.engcreatesemaphore, gdifncs_d0ae1b52-59e6-49a9-ab03-7ff1008dc5c6.xml, winddi/EngCreateSemaphore
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	EngCreateSemaphore
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngCreateSemaphore function


## -description


The <b>EngCreateSemaphore</b> function creates a semaphore object.


## -parameters






## -returns



If the function succeeds, the return value is a handle to the semaphore object. A null pointer is returned if the function fails.




## -remarks



Graphics drivers can create and use a semaphore object for resource synchronization. For example:

<ul>
<li>
The <i>Permedia</i> display driver uses a semaphore when an asynchronous pointer requires access to the CRTC registers, because these registers are shared by both the asynchronous hardware pointers and the synchronous activities of the device.

</li>
<li>
Multiple printer drivers sharing global data, such as font data on a print server, need to synchronize access to this data.

</li>
</ul>
<div class="alert"><b>Note</b>  The Microsoft Windows Driver Kit (WDK) does not contain the 3Dlabs Permedia2 (<i>3dlabs.htm</i> ) and 3Dlabs Permedia3 (<i>Perm3.htm</i>) sample display drivers. You can get these sample drivers from the Windows Server 2003 SP1 Driver Development Kit (DDK), which you can download from the <a href="http://go.microsoft.com/fwlink/p/?linkid=21859">DDK - Windows Driver Development Kit</a> page of the WDHC website.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564819">EngDeleteSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564960">EngIsSemaphoreOwned</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564961">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a>
 

 

