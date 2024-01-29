---
UID: NF:psapi.EnumDeviceDrivers
title: EnumDeviceDrivers function (psapi.h)
description: Retrieves the load address for each device driver in the system.
helpviewer_keywords: ["EnumDeviceDrivers","EnumDeviceDrivers function [PSAPI]","K32EnumDeviceDrivers","_win32_enumdevicedrivers","base.enumdevicedrivers","psapi.enumdevicedrivers","psapi/EnumDeviceDrivers","psapi/K32EnumDeviceDrivers"]
old-location: psapi\enumdevicedrivers.htm
tech.root: psapi
ms.assetid: 55925741-da23-44b1-93e8-0e9468434a61
ms.date: 12/05/2018
ms.keywords: EnumDeviceDrivers, EnumDeviceDrivers function [PSAPI], K32EnumDeviceDrivers, _win32_enumdevicedrivers, base.enumdevicedrivers, psapi.enumdevicedrivers, psapi/EnumDeviceDrivers, psapi/K32EnumDeviceDrivers
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumDeviceDrivers
 - psapi/EnumDeviceDrivers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - Psapi.dll
 - Psapi.dll
 - API-MS-Win-Core-PsAPI-L1-1-0.dll
 - KernelBase.dll
api_name:
 - EnumDeviceDrivers
 - K32EnumDeviceDrivers
---

# EnumDeviceDrivers function


## -description

Retrieves the load address for each device driver in the system.

## -parameters

### -param lpImageBase [out]

An array that receives the list of load addresses for the device drivers.

### -param cb [in]

The size of the <i>lpImageBase</i> array, in bytes. If the array is not large enough to store the load addresses, the <i>lpcbNeeded</i> parameter receives the required size of the array.

### -param lpcbNeeded [out]

The number of bytes returned in the <i>lpImageBase</i> array.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To determine how many device drivers were enumerated by the call to 
<b>EnumDeviceDrivers</b>, divide the resulting value in the <i>lpcbNeeded</i> parameter by <code>sizeof(LPVOID)</code>.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes version numbers for the PSAPI functions. The PSAPI version number affects  the name used to call the function and the library that a program must load. 

If PSAPI_VERSION is 2 or greater, this function is defined as <b>K32EnumDeviceDrivers</b> in Psapi.h and exported in Kernel32.lib and Kernel32.dll. If PSAPI_VERSION is 1, this function is defined as <b>EnumDeviceDrivers</b> in Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls <b>K32EnumDeviceDrivers</b>. 

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions should always call this function as <b>EnumDeviceDrivers</b>. To ensure correct resolution of symbols, add Psapi.lib to the TARGETLIBS macro and compile the program with –DPSAPI_VERSION=1. To use run-time dynamic linking, load Psapi.dll.

Starting in Windows 11 Version 24H2, <b>EnumDeviceDrivers</b> will require <b>SeDebugPrivilege</b> to return valid <i>ImageBase</i> values. The function will still succeed if the caller does not have this privilege enabled, but the returned <i>lpImageBase</i> array will contain addresses that are all NULL.


#### Examples

For an example, see <a href="/windows/desktop/psapi/enumerating-all-device-drivers-in-the-system">Enumerating all Device Drivers in the System</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/psapi/device-driver-information">Device Driver Information</a>



<a href="/windows/desktop/api/psapi/nf-psapi-getdevicedriverbasenamea">GetDeviceDriverBaseName</a>



<a href="/windows/desktop/api/psapi/nf-psapi-getdevicedriverfilenamea">GetDeviceDriverFileName</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>