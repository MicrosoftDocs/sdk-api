---
UID: NF:winddi.EngGetCurrentThreadId
title: EngGetCurrentThreadId function
author: windows-sdk-content
description: The EngGetCurrentThreadId function identifies an application's current thread.
old-location: display\enggetcurrentthreadid.htm
tech.root: display
ms.assetid: f1fdb223-b649-4467-a4c4-56cce4f4d975
ms.author: windowssdkdev
ms.date: 10/19/2018
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: Any level
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngGetCurrentThreadId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/63ed7f38-6874-4d33-80e4-fdd00175e039">EngGetCurrentProcessId</a>



<a href="https://msdn.microsoft.com/51e39335-8ad7-4cd9-b46b-6fdd7a4de0bf">EngGetProcessHandle</a>
 

 

