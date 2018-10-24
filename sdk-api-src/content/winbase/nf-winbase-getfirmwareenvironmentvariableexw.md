---
UID: NF:winbase.GetFirmwareEnvironmentVariableExW
title: GetFirmwareEnvironmentVariableExW function
author: windows-sdk-content
description: Retrieves the value of the specified firmware environment variable and its attributes.
old-location: base\getfirmwareenvironmentvariableex.htm
tech.root: sysinfo
ms.assetid: B093BA68-C68B-4ED6-9902-058650A191FD
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetFirmwareEnvironmentVariableEx, GetFirmwareEnvironmentVariableEx function, GetFirmwareEnvironmentVariableExA, GetFirmwareEnvironmentVariableExW, base.getfirmwareenvironmentvariableex, winbase/GetFirmwareEnvironmentVariableEx, winbase/GetFirmwareEnvironmentVariableExA, winbase/GetFirmwareEnvironmentVariableExW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFirmwareEnvironmentVariableExW (Unicode) and GetFirmwareEnvironmentVariableExA (ANSI)
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
 - API-MS-Win-Core-firmware-l1-1-0.dll
 - kernel32legacy.dll
api_name:
 - GetFirmwareEnvironmentVariableEx
 - GetFirmwareEnvironmentVariableExA
 - GetFirmwareEnvironmentVariableExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFirmwareEnvironmentVariableExW function


## -description


Retrieves the value of the specified firmware environment variable and its attributes.


## -parameters




### -param lpName

The name of the firmware environment variable. The pointer must not be <b>NULL</b>.


### -param lpGuid

The GUID that represents the namespace of the firmware environment variable. The GUID must be  a string in the format  "{<i>xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx</i>}" where 'x' represents a hexadecimal value. The pointer must not be <b>NULL</b>.


### -param pBuffer

A pointer to a buffer that receives the value of the specified firmware environment variable.


### -param nSize

The size of the <i>pValue</i> buffer, in bytes.


### -param pdwAttribubutes

Bitmask identifying UEFI variable attributes associated with the variable. See <a href="https://msdn.microsoft.com/D3C2F03F-66F6-40A4-830E-058BBA925ACD">SetFirmwareEnvironmentVariableEx</a> for the bitmask definition.


## -returns



If the function succeeds, the return value is the number of bytes stored in the <i>pValue</i> buffer.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error codes include ERROR_INVALID_FUNCTION.




## -remarks



Starting with Windows 10, version 1803, Universal Windows apps can read and write UEFI firmware variables. See <a href="https://msdn.microsoft.com/en-us/library/Mt829375(v=VS.85).aspx">Access UEFI firmware variables from a Universal Windows App</a>for details.

To read a UEFI firmware environment variable, the user account that the app is running under must have the <a href="https://msdn.microsoft.com/library/windows/desktop/bb530716(v=vs.85).aspx">SE_SYSTEM_ENVIRONMENT_NAME</a> privilege. A Universal Windows app must be run from an administrator account and follow the requirements outlined in <a href="https://msdn.microsoft.com/en-us/library/Mt829375(v=VS.85).aspx">Access UEFI firmware variables from a Universal Windows App</a>.

Starting with Windows 10, version 1803, reading Unified Extensible Firmware Interface (UEFI) variables is also supported from User-Mode Driver Framework (UMDF) drivers. Writing UEFI variables from UMDF drivers is not supported.

The exact set of firmware environment variables is determined by the boot firmware. The location of these environment variables is also specified by the firmware.  For example, on a UEFI-based system, NVRAM contains firmware environment variables that specify system boot settings. For information about specific variables used, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=183072">UEFI specification</a>. For more information about UEFI and Windows, see <a href="http://go.microsoft.com/fwlink/p/?linkid=183071">UEFI and Windows</a>.

Firmware variables are not supported on a legacy BIOS-based system. The <b>GetFirmwareEnvironmentVariableEx</b> function will always fail on a legacy BIOS-based system, or if Windows was installed using legacy BIOS on a system that supports both legacy BIOS and UEFI. To identify these conditions, call the function with a dummy firmware environment name such as an empty string ("") for the <i>lpName</i> parameter and a dummy GUID such as "{00000000-0000-0000-0000-000000000000}" for the <i>lpGuid</i> parameter. On a legacy BIOS-based system, or on a system that supports both legacy BIOS and UEFI where Windows was installed using legacy BIOS, the function will fail with  ERROR_INVALID_FUNCTION. On a UEFI-based system, the function will  fail with an error specific to the firmware, such as ERROR_NOACCESS, to indicate that the dummy GUID namespace does not exist. 

If you are creating a backup application, you can use this function to save all the boot settings for the system so they can be restored using the <a href="https://msdn.microsoft.com/42117632-61aa-4f83-abe1-c08f40cf3f0a">SetFirmwareEnvironmentVariable</a> 
	 function if needed. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt829375(v=VS.85).aspx">Access UEFI firmware variables from a Universal Windows App</a>



<a href="https://msdn.microsoft.com/18e74e54-ecfe-46bf-8c9d-9eb16d22f3ba">GetFirmwareEnvironmentVariable</a>



<a href="https://msdn.microsoft.com/D3C2F03F-66F6-40A4-830E-058BBA925ACD">SetFirmwareEnvironmentVariableEx</a>
 

 

