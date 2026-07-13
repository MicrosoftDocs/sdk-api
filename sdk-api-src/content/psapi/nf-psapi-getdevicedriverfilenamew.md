---
UID: NF:psapi.GetDeviceDriverFileNameW
title: GetDeviceDriverFileNameW function (psapi.h)
description: Retrieves the path available for the specified device driver. (Unicode)
helpviewer_keywords: ["GetDeviceDriverFileName", "GetDeviceDriverFileName function [PSAPI]", "GetDeviceDriverFileNameW", "K32GetDeviceDriverFileName", "K32GetDeviceDriverFileNameW", "_win32_getdevicedriverfilename", "base.getdevicedriverfilename", "psapi.getdevicedriverfilename", "psapi/GetDeviceDriverFileName", "psapi/GetDeviceDriverFileNameW", "psapi/K32GetDeviceDriverFileName", "psapi/K32GetDeviceDriverFileNameW"]
old-location: psapi\getdevicedriverfilename.htm
tech.root: psapi
ms.assetid: 6ddbcf7e-e41c-4ea7-b60a-01ed5c98c530
ms.date: 12/05/2018
ms.keywords: GetDeviceDriverFileName, GetDeviceDriverFileName function [PSAPI], GetDeviceDriverFileNameA, GetDeviceDriverFileNameW, K32GetDeviceDriverFileName, K32GetDeviceDriverFileNameA, K32GetDeviceDriverFileNameW, _win32_getdevicedriverfilename, base.getdevicedriverfilename, psapi.getdevicedriverfilename, psapi/GetDeviceDriverFileName, psapi/GetDeviceDriverFileNameA, psapi/GetDeviceDriverFileNameW, psapi/K32GetDeviceDriverFileName, psapi/K32GetDeviceDriverFileNameA, psapi/K32GetDeviceDriverFileNameW
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDeviceDriverFileNameW (Unicode) and GetDeviceDriverFileNameA (ANSI)
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
 - GetDeviceDriverFileNameW
 - psapi/GetDeviceDriverFileNameW
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
 - API-MS-Win-Core-PsAPI-Ansi-L1-1-0.dll
 - API-MS-Win-Core-PsAPI-L1-1-0.dll
 - KernelBase.dll
api_name:
 - GetDeviceDriverFileName
 - GetDeviceDriverFileNameA
 - GetDeviceDriverFileNameW
 - K32GetDeviceDriverFileName
 - K32GetDeviceDriverFileNameW
 - K32GetDeviceDriverFileNameA
---

# GetDeviceDriverFileNameW function


## -description

Retrieves the path available for the specified device driver.

## -parameters

### -param ImageBase [in]

The load address of the device driver.

### -param lpFilename [out]

A pointer to the buffer that receives the path to the device driver.

### -param nSize [in]

The size of the <i>lpFilename</i> buffer, in characters. If the buffer is not large enough to store the path plus the terminating null character, the string is truncated.

## -returns

If the function succeeds, the return value specifies the length of the string copied to the buffer, not including any terminating null character.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes version numbers for the PSAPI functions. The PSAPI version number affects  the name used to call the function and the library that a program must load. 

If PSAPI_VERSION is 2 or greater, this function is defined as <b>K32GetDeviceDriverFileName</b> in Psapi.h and exported in Kernel32.lib and Kernel32.dll. If PSAPI_VERSION is 1, this function is defined as <b>GetDeviceDriverFileName</b> in Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls <b>K32GetDeviceDriverFileName</b>. 

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions should always call this function as <b>GetDeviceDriverFileName</b>. To ensure correct resolution of symbols, add Psapi.lib to the TARGETLIBS macro and compile the program with –DPSAPI_VERSION=1. To use run-time dynamic linking, load Psapi.dll.





> [!NOTE]
> The psapi.h header defines GetDeviceDriverFileName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/psapi/device-driver-information">Device Driver Information</a>



<a href="/windows/desktop/api/psapi/nf-psapi-enumdevicedrivers">EnumDeviceDrivers</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>
