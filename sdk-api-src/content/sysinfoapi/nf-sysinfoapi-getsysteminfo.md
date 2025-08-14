---
UID: NF:sysinfoapi.GetSystemInfo
title: GetSystemInfo function (sysinfoapi.h)
description: Retrieves information about the current system.
helpviewer_keywords: ["GetSystemInfo","GetSystemInfo function","_win32_getsysteminfo","base.getsysteminfo","sysinfoapi/GetSystemInfo"]
old-location: base\getsysteminfo.htm
tech.root: winprog
ms.assetid: f6d745af-729a-494e-90b4-19fe7d97c7af
ms.date: 12/05/2018
ms.keywords: GetSystemInfo, GetSystemInfo function, _win32_getsysteminfo, base.getsysteminfo, sysinfoapi/GetSystemInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSystemInfo
 - sysinfoapi/GetSystemInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
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
---

# GetSystemInfo function


## -description

Retrieves information about the current system.

To retrieve accurate information for an application running on WOW64, call the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo">GetNativeSystemInfo</a> function.

## -parameters

### -param lpSystemInfo [out]

A pointer to a 
<a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a> structure that receives the information.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo">GetNativeSystemInfo</a>



<a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>