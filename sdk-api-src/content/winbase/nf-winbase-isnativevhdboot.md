---
UID: NF:winbase.IsNativeVhdBoot
title: IsNativeVhdBoot function
author: windows-sdk-content
description: Indicates if the OS was booted from a VHD container.
old-location: base\isnativevhdboot.htm
old-project: SysInfo
ms.assetid: 8198D4AF-553D-42B3-AF22-EC2C63C0E9AE
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IsNativeVhdBoot, IsNativeVhdBoot , IsNativeVhdBoot function, base.isnativevhdboot, base.isnativevhdboot_, winbase/IsNativeVhdBoot
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - IsNativeVhdBoot
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IsNativeVhdBoot function


## -description


Indicates if the OS was booted from a VHD container.


## -parameters




### -param NativeVhdBoot [out]

Pointer to a variable that receives a boolean
        indicating if the OS was booted from a VHD.


## -returns



TRUE if the OS was a native VHD boot; otherwise, FALSE.

Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to get extended error information.




## -see-also




<a href="https://msdn.microsoft.com/bb8cf86b-00b8-4a64-90f8-66ac6dbf9dee">GetProcessHandleCount</a>



<a href="https://msdn.microsoft.com/12990e8d-6097-4502-824e-db6c3f76c715">GetProcessMemoryInfo</a>



<a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a>



<a href="https://msdn.microsoft.com/06687b2a-2dab-4102-8022-4b70677064b2">GetSystemRegistryQuota</a>



<a href="https://msdn.microsoft.com/84f674e7-536b-4ae0-b523-6a17cb0a1c17">GetSystemTimes</a>
 

 

