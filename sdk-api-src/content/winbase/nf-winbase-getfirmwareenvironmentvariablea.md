---
UID: NF:winbase.GetFirmwareEnvironmentVariableA
title: GetFirmwareEnvironmentVariableA function
author: windows-sdk-content
description: Retrieves the value of the specified firmware environment variable.
old-location: base\getfirmwareenvironmentvariable.htm
tech.root: SysInfo
ms.assetid: 18e74e54-ecfe-46bf-8c9d-9eb16d22f3ba
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetFirmwareEnvironmentVariable, GetFirmwareEnvironmentVariable function, GetFirmwareEnvironmentVariableA, GetFirmwareEnvironmentVariableW, base.getfirmwareenvironmentvariable, winbase/GetFirmwareEnvironmentVariable, winbase/GetFirmwareEnvironmentVariableA, winbase/GetFirmwareEnvironmentVariableW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFirmwareEnvironmentVariableW (Unicode) and GetFirmwareEnvironmentVariableA (ANSI)
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
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
api_name:
 - GetFirmwareEnvironmentVariable
 - GetFirmwareEnvironmentVariableA
 - GetFirmwareEnvironmentVariableW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFirmwareEnvironmentVariableA function


## -description


Retrieves the value of the specified firmware environment variable.


## -parameters




### -param lpName [in]

The name of the firmware environment variable. The pointer must not be <b>NULL</b>.


### -param lpGuid [in]

The GUID that represents the namespace of the firmware environment variable. The GUID must be  a string in the format  "{<i>xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx</i>}" where 'x' represents a hexadecimal value. 


### -param pBuffer [out]

A pointer to a buffer that receives the value of the specified firmware environment variable.


### -param nSize [in]

The size of the <i>pBuffer</i> buffer, in bytes.


## -returns



If the function succeeds, the return value is the number of bytes stored in the <i>pBuffer</i> buffer.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error codes include ERROR_INVALID_FUNCTION.




## -remarks



Starting with Windows 10, version 1803, Universal Windows apps can read and write Unified Extensible Firmware Interface (UEFI) firmware variables. See <a href="https://msdn.microsoft.com/en-us/library/Mt829375(v=VS.85).aspx">Access UEFI firmware variables from a Universal Windows App</a>for details.

To read a firmware environment variable, the user account that the app is running under must have the <a href="https://msdn.microsoft.com/library/windows/desktop/bb530716(v=vs.85).aspx">SE_SYSTEM_ENVIRONMENT_NAME</a> privilege. A Universal Windows app must be run from an administrator account and follow the requirements outlined in <a href="https://msdn.microsoft.com/en-us/library/Mt829375(v=VS.85).aspx">Access UEFI firmware variables from a Universal Windows App</a>.

Starting with Windows 10, version 1803, reading Unified Extensible Firmware Interface (UEFI) variables is also supported from User-Mode Driver Framework (UMDF) drivers. Writing UEFI variables from UMDF drivers is not supported.

The exact set of firmware environment variables is determined by the boot firmware. The location of these environment variables is also specified by the firmware.  For example, on a UEFI-based system, NVRAM contains firmware environment variables that specify system boot settings. For information about specific variables used, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=183072">UEFI specification</a>. For more information about UEFI and Windows, see <a href="http://go.microsoft.com/fwlink/p/?linkid=183071">UEFI and Windows</a>.

Firmware variables are not supported on a legacy BIOS-based system. The <b>GetFirmwareEnvironmentVariable</b> function will always fail on a legacy BIOS-based system, or if Windows was installed using legacy BIOS on a system that supports both legacy BIOS and UEFI. To identify these conditions, call the function with a dummy firmware environment name such as an empty string ("") for the <i>lpName</i> parameter and a dummy GUID such as "{00000000-0000-0000-0000-000000000000}" for the <i>lpGuid</i> parameter. On a legacy BIOS-based system, or on a system that supports both legacy BIOS and UEFI where Windows was installed using legacy BIOS, the function will fail with  ERROR_INVALID_FUNCTION. On a UEFI-based system, the function will  fail with an error specific to the firmware, such as ERROR_NOACCESS, to indicate that the dummy GUID namespace does not exist. 

If you are creating a backup application, you can use this function to save all the boot settings for the system so they can be restored using the <a href="https://msdn.microsoft.com/42117632-61aa-4f83-abe1-c08f40cf3f0a">SetFirmwareEnvironmentVariable</a> 
	 function if needed. 

<b>GetFirmwareEnvironmentVariable</b> is the user-mode equivalent of the <a href="https://msdn.microsoft.com/5AD76955-A44C-4231-9394-0B6595CFB33D">ExGetFirmwareEnvironmentVariable</a> kernel-mode routine.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt829375(v=VS.85).aspx">Access UEFI firmware variables from a Universal Windows App</a>



<a href="https://msdn.microsoft.com/B093BA68-C68B-4ED6-9902-058650A191FD">GetFirmwareEnvironmentVariableEx</a>



<a href="https://msdn.microsoft.com/42117632-61aa-4f83-abe1-c08f40cf3f0a">SetFirmwareEnvironmentVariable</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System
		  Information Functions</a>
 

 

