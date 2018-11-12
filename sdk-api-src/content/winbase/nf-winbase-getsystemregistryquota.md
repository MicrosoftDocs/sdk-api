---
UID: NF:winbase.GetSystemRegistryQuota
title: GetSystemRegistryQuota function
author: windows-sdk-content
description: Retrieves the current size of the registry and the maximum size that the registry is allowed to attain on the system.
old-location: base\getsystemregistryquota.htm
tech.root: sysinfo
ms.assetid: 06687b2a-2dab-4102-8022-4b70677064b2
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetSystemRegistryQuota, GetSystemRegistryQuota function, base.getsystemregistryquota, winbase/GetSystemRegistryQuota
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetSystemRegistryQuota
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemRegistryQuota function


## -description


Retrieves the current size of the registry and the  maximum size that the registry is allowed to attain on the system.


## -parameters




### -param pdwQuotaAllowed [out, optional]

A pointer to a variable that receives the maximum size that the registry is allowed to attain on this system, in bytes.


### -param pdwQuotaUsed [out, optional]

A pointer to a variable that receives the current size of  the registry, in bytes.


## -returns



If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System Information Functions</a>
 

 

