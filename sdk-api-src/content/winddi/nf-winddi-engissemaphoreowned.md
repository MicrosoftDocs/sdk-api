---
UID: NF:winddi.EngIsSemaphoreOwned
title: EngIsSemaphoreOwned function
author: windows-sdk-content
description: The EngIsSemaphoreOwned function determines whether any thread holds the specified semaphore.
old-location: display\engissemaphoreowned.htm
old-project: display
ms.assetid: a04f6f46-f075-40d1-8b56-d37a80fb3571
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EngIsSemaphoreOwned, EngIsSemaphoreOwned function [Display Devices], display.engissemaphoreowned, gdifncs_9bf4c866-a563-4bc5-99d6-0189f10f0742.xml, winddi/EngIsSemaphoreOwned
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
 - EngIsSemaphoreOwned
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngIsSemaphoreOwned function


## -description


The <b>EngIsSemaphoreOwned</b> function determines whether any thread holds the specified semaphore.


## -parameters




### -param hsem [in]

Handle to the semaphore.


## -returns



<b>EngIsSemaphoreOwned</b> returns <b>TRUE</b> if any thread holds the specified semaphore, and <b>FALSE</b> if no thread holds it.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564760">EngCreateSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564961">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a>
 

 

