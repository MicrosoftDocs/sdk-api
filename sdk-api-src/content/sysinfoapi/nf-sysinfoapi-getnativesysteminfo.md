---
UID: NF:sysinfoapi.GetNativeSystemInfo
title: GetNativeSystemInfo function (sysinfoapi.h)
description: Retrieves information about the current system to an application running under WOW64.helpviewer_keywords: ["GetNativeSystemInfo","GetNativeSystemInfo function","_win32_getnativesysteminfo","base.getnativesysteminfo","sysinfoapi/GetNativeSystemInfo"]
old-location: base\getnativesysteminfo.htm
tech.root: SysInfo
ms.assetid: a4a1123b-83d7-4ee2-aa38-68fff5373618
ms.date: 12/05/2018
ms.keywords: GetNativeSystemInfo, GetNativeSystemInfo function, _win32_getnativesysteminfo, base.getnativesysteminfo, sysinfoapi/GetNativeSystemInfo
f1_keywords:
- sysinfoapi/GetNativeSystemInfo
dev_langs:
- c++
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
- API-MS-Win-Core-SysInfo-l1-2-0.dll
- KernelBase.dll
- API-MS-Win-Core-SysInfo-l1-2-1.dll
- API-MS-Win-Core-SysInfo-l1-2-2.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
- API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
- GetNativeSystemInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetNativeSystemInfo function


## -description


Retrieves information about the current system to an application running under 
<a href="https://docs.microsoft.com/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a>. If the function is called from a 64-bit application, or on a 64-bit system that does not have an Intel64 or x64 processor (such as ARM64), it is equivalent to the 
<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function.


## -parameters




### -param lpSystemInfo [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a> structure that receives the information.


## -remarks



To determine whether a Win32-based application is running under WOW64, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2">IsWow64Process2</a> function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/SysInfo/getting-the-system-version">Getting the System Version</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process">IsWow64Process</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>
 

 

