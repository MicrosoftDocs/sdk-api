---
UID: NF:psapi.GetDeviceDriverBaseNameW
title: GetDeviceDriverBaseNameW function (psapi.h)
description: Retrieves the base name of the specified device driver.helpviewer_keywords: ["GetDeviceDriverBaseName","GetDeviceDriverBaseName function [PSAPI]","GetDeviceDriverBaseNameA","GetDeviceDriverBaseNameW","K32GetDeviceDriverBaseName","K32GetDeviceDriverBaseNameA","K32GetDeviceDriverBaseNameW","_win32_getdevicedriverbasename","base.getdevicedriverbasename","psapi.getdevicedriverbasename","psapi/GetDeviceDriverBaseName","psapi/GetDeviceDriverBaseNameA","psapi/GetDeviceDriverBaseNameW","psapi/K32GetDeviceDriverBaseName","psapi/K32GetDeviceDriverBaseNameA","psapi/K32GetDeviceDriverBaseNameW"]
old-location: psapi\getdevicedriverbasename.htm
tech.root: psapi
ms.assetid: a19a927d-4669-4d4c-951e-43f294a8fb40
ms.date: 12/05/2018
ms.keywords: GetDeviceDriverBaseName, GetDeviceDriverBaseName function [PSAPI], GetDeviceDriverBaseNameA, GetDeviceDriverBaseNameW, K32GetDeviceDriverBaseName, K32GetDeviceDriverBaseNameA, K32GetDeviceDriverBaseNameW, _win32_getdevicedriverbasename, base.getdevicedriverbasename, psapi.getdevicedriverbasename, psapi/GetDeviceDriverBaseName, psapi/GetDeviceDriverBaseNameA, psapi/GetDeviceDriverBaseNameW, psapi/K32GetDeviceDriverBaseName, psapi/K32GetDeviceDriverBaseNameA, psapi/K32GetDeviceDriverBaseNameW
f1_keywords:
- psapi/GetDeviceDriverBaseName
dev_langs:
- c++
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDeviceDriverBaseNameW (Unicode) and GetDeviceDriverBaseNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- Psapi.dll
- Psapi.dll
- API-MS-Win-Core-PsAPI-Ansi-L1-1-0.dll
- API-MS-Win-Core-PsAPI-L1-1-0.dll
- KernelBase.dll
api_name:
- GetDeviceDriverBaseName
- GetDeviceDriverBaseNameA
- GetDeviceDriverBaseNameW
- K32GetDeviceDriverBaseName
- K32GetDeviceDriverBaseNameW
- K32GetDeviceDriverBaseNameA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetDeviceDriverBaseNameW function


## -description


Retrieves the base name of the specified device driver.


## -parameters




### -param ImageBase [in]

The load address of the device driver. This value can be retrieved using the 
      <a href="https://docs.microsoft.com/windows/desktop/api/psapi/nf-psapi-enumdevicedrivers">EnumDeviceDrivers</a> 
      function.


#### - lpBaseName [out]

A pointer to the buffer that receives the base name of the device driver.


### -param nSize [in]

The size of the <i>lpBaseName</i> buffer, in characters. If the buffer is not large enough to store the base name plus the terminating null character, the string is truncated.


## -returns



If the function succeeds, the return value specifies the length of the string copied to the buffer, not including any terminating null character.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes version numbers for the PSAPI functions. The PSAPI version number affects  the name used to call the function and the library that a program must load.

If PSAPI_VERSION is 2 or greater, this function is defined as <b>K32GetDeviceDriverBaseName</b> in Psapi.h and exported in Kernel32.lib and Kernel32.dll. If PSAPI_VERSION is 1, this function is defined as <b>GetDeviceDriverBaseName</b> in Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls <b>K32GetDeviceDriverBaseName</b>.

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions should always call this function as <b>GetDeviceDriverBaseName</b>. To ensure correct resolution of symbols, add Psapi.lib to the TARGETLIBS macro and compile the program with –DPSAPI_VERSION=1. To use run-time dynamic linking, load Psapi.dll.


#### Examples

For an example, see 
     <a href="https://docs.microsoft.com/windows/desktop/psapi/enumerating-all-device-drivers-in-the-system">Enumerating all Device Drivers in the System</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/psapi/device-driver-information">Device Driver Information</a>



<a href="https://docs.microsoft.com/windows/desktop/api/psapi/nf-psapi-enumdevicedrivers">EnumDeviceDrivers</a>



<a href="https://docs.microsoft.com/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>
 

 

