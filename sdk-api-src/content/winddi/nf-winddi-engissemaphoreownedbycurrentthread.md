---
UID: NF:winddi.EngIsSemaphoreOwnedByCurrentThread
title: EngIsSemaphoreOwnedByCurrentThread function
author: windows-sdk-content
description: The EngIsSemaphoreOwnedByCurrentThread function determines whether the currently executing thread holds the specified semaphore.
old-location: display\engissemaphoreownedbycurrentthread.htm
old-project: display
ms.assetid: ce5d8ceb-0137-4ca9-b718-2e3de650249d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EngIsSemaphoreOwnedByCurrentThread, EngIsSemaphoreOwnedByCurrentThread function [Display Devices], display.engissemaphoreownedbycurrentthread, gdifncs_6c3dcc33-1798-4dc5-a64f-a9bb85f5cf81.xml, winddi/EngIsSemaphoreOwnedByCurrentThread
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
 - EngIsSemaphoreOwnedByCurrentThread
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngIsSemaphoreOwnedByCurrentThread function


## -description


The <b>EngIsSemaphoreOwnedByCurrentThread</b> function determines whether the currently executing thread holds the specified semaphore.


## -parameters




### -param hsem [in]

Handle to the semaphore.


## -returns



<b>EngIsSemaphoreOwnedByCurrentThread</b> returns <b>TRUE</b> if the currently executing thread holds the specified semaphore, and <b>FALSE</b> if it does not.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564760">EngCreateSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564960">EngIsSemaphoreOwned</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a>
 

 

