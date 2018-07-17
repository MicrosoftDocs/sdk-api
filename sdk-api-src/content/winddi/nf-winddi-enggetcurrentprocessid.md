---
UID: NF:winddi.EngGetCurrentProcessId
title: EngGetCurrentProcessId function
author: windows-sdk-content
description: The EngGetCurrentProcessId function identifies an application's current process.
old-location: display\enggetcurrentprocessid.htm
old-project: display
ms.assetid: 63ed7f38-6874-4d33-80e4-fdd00175e039
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: EngGetCurrentProcessId, EngGetCurrentProcessId function [Display Devices], display.enggetcurrentprocessid, gdifncs_073e5c03-16d4-4257-bf0a-7ea183beea9d.xml, winddi/EngGetCurrentProcessId
ms.prod: windows
ms.technology: windows-sdk
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
 - EngGetCurrentProcessId
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: Any level
req.product: Windows Address Book 5.0
---

# EngGetCurrentProcessId function


## -description


The <b>EngGetCurrentProcessId</b> function identifies an application's current process.


## -parameters






## -returns



<b>EngGetCurrentProcessId</b> returns the 4-byte identifier of the application's process.




## -remarks



Callers of <b>EngGetCurrentProcessId</b> should treat the returned ID as a read-only value. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564922">EngGetCurrentThreadId</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564955">EngGetProcessHandle</a>
 

 

