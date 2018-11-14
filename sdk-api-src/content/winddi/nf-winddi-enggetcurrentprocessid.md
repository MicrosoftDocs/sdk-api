---
UID: NF:winddi.EngGetCurrentProcessId
title: EngGetCurrentProcessId function
author: windows-sdk-content
description: The EngGetCurrentProcessId function identifies an application's current process.
old-location: display\enggetcurrentprocessid.htm
tech.root: display
ms.assetid: 63ed7f38-6874-4d33-80e4-fdd00175e039
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: EngGetCurrentProcessId, EngGetCurrentProcessId function [Display Devices], display.enggetcurrentprocessid, gdifncs_073e5c03-16d4-4257-bf0a-7ea183beea9d.xml, winddi/EngGetCurrentProcessId
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
 - EngGetCurrentProcessId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EngGetCurrentProcessId
: 
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




<a href="https://msdn.microsoft.com/f1fdb223-b649-4467-a4c4-56cce4f4d975">EngGetCurrentThreadId</a>



<a href="https://msdn.microsoft.com/51e39335-8ad7-4cd9-b46b-6fdd7a4de0bf">EngGetProcessHandle</a>
 

 

