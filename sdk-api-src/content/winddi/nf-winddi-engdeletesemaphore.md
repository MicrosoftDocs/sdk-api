---
UID: NF:winddi.EngDeleteSemaphore
title: EngDeleteSemaphore function
author: windows-sdk-content
description: The EngDeleteSemaphore function deletes a semaphore object from the system's resource list.
old-location: display\engdeletesemaphore.htm
old-project: display
ms.assetid: 6855017c-8919-496b-b82c-d65dea7ad5f0
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: EngDeleteSemaphore, EngDeleteSemaphore function [Display Devices], display.engdeletesemaphore, gdifncs_a669ceb3-f9b3-4940-b1f8-17c55ee42f59.xml, winddi/EngDeleteSemaphore
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngDeleteSemaphore
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngDeleteSemaphore function


## -description


The <b>EngDeleteSemaphore</b> function deletes a semaphore object from the system's resource list.


## -parameters




### -param hsem [in]

Handle to the semaphore to be deleted. The semaphore was created in <a href="https://msdn.microsoft.com/library/windows/hardware/ff564760">EngCreateSemaphore</a>.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564760">EngCreateSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a>
 

 

