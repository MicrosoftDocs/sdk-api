---
UID: NF:sysinfoapi.GetSystemInfo
title: GetSystemInfo function (sysinfoapi.h)
author: windows-sdk-content
description: Retrieves information about the current system.
old-location: base\getsysteminfo.htm
tech.root: SysInfo
ms.assetid: f6d745af-729a-494e-90b4-19fe7d97c7af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSystemInfo, GetSystemInfo function, _win32_getsysteminfo, base.getsysteminfo, sysinfoapi/GetSystemInfo
ms.topic: function
f1_keywords: ["sysinfoapi/GetSystemInfo"]
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetSystemInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetSystemInfo function


## -description


Retrieves information about the current system.

To retrieve accurate information for an application running on WOW64, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo">GetNativeSystemInfo</a> function.


## -parameters




### -param lpSystemInfo [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/ns-sysinfoapi-_system_info">SYSTEM_INFO</a> structure that receives the information.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo">GetNativeSystemInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/ns-sysinfoapi-_system_info">SYSTEM_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>
 

 

