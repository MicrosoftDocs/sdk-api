---
UID: NF:winbase.IsNativeVhdBoot
title: IsNativeVhdBoot function (winbase.h)

description: Indicates if the OS was booted from a VHD container.
old-location: base\isnativevhdboot.htm
tech.root: SysInfo
ms.assetid: 8198D4AF-553D-42B3-AF22-EC2C63C0E9AE

ms.date: 12/05/2018
ms.keywords: IsNativeVhdBoot, IsNativeVhdBoot , IsNativeVhdBoot function, base.isnativevhdboot, base.isnativevhdboot_, winbase/IsNativeVhdBoot
ms.topic: function
f1_keywords: 
 - "winbase/IsNativeVhdBoot"
dev_langs:
 - c++
req.header: winbase.h
req.include-header: Windows.h
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
 - IsNativeVhdBoot
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount">GetProcessHandleCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getsystemregistryquota">GetSystemRegistryQuota</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getsystemtimes">GetSystemTimes</a>
 

 

