---
UID: NF:winddi.EngGetCurrentThreadId
title: EngGetCurrentThreadId function
author: windows-driver-content
description: The EngGetCurrentThreadId function identifies an application's current thread.
old-location: display\enggetcurrentthreadid.htm
old-project: display
ms.assetid: f1fdb223-b649-4467-a4c4-56cce4f4d975
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: EngGetCurrentThreadId, EngGetCurrentThreadId function [Display Devices], display.enggetcurrentthreadid, gdifncs_f6b5f95d-aa1b-4ff9-8523-79f6e2baef9d.xml, winddi/EngGetCurrentThreadId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: This function is available in Windows XP and later.
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
api_name:
-	EngGetCurrentThreadId
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: Any level
req.product: Windows Address Book 5.0
---

# EngGetCurrentThreadId function


## -description


The <b>EngGetCurrentThreadId</b> function identifies an application's current thread.


## -parameters






## -returns



<b>EngGetCurrentThreadId</b> returns the 4-byte identifier of the application's thread.




## -remarks



Callers of <b>EngGetCurrentThreadId</b> should treat the returned ID as a read-only value. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564919">EngGetCurrentProcessId</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564955">EngGetProcessHandle</a>
 

 

