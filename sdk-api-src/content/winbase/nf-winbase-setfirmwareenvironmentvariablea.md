---
UID: NF:winbase.SetFirmwareEnvironmentVariableA
title: SetFirmwareEnvironmentVariableA function (winbase.h)
author: windows-sdk-content
description: Sets the value of the specified firmware environment variable.
old-location: base\setfirmwareenvironmentvariable.htm
tech.root: SysInfo
ms.assetid: 42117632-61aa-4f83-abe1-c08f40cf3f0a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetFirmwareEnvironmentVariable, SetFirmwareEnvironmentVariable function, SetFirmwareEnvironmentVariableA, SetFirmwareEnvironmentVariableW, base.setfirmwareenvironmentvariable, winbase/SetFirmwareEnvironmentVariable, winbase/SetFirmwareEnvironmentVariableA, winbase/SetFirmwareEnvironmentVariableW
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetFirmwareEnvironmentVariableW (Unicode) and SetFirmwareEnvironmentVariableA (ANSI)
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
 - SetFirmwareEnvironmentVariable
 - SetFirmwareEnvironmentVariableA
 - SetFirmwareEnvironmentVariableW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetFirmwareEnvironmentVariableA function


## -description


Sets the value of the specified firmware environment variable.


## -parameters




### -param lpName [in]

The name of the firmware environment variable. The pointer must not be <b>NULL</b>.


### -param lpGuid [in]

The GUID that represents the namespace of the firmware environment variable. The GUID must be a string in the format  "{<i>xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx</i>}". If the system does not support GUID-based namespaces, this parameter is ignored.


### -param pValue [in]

A pointer to the new value for the  firmware environment variable.


### -param nSize [in]

The size of the <i>pBuffer</i> buffer, in bytes. If this parameter is zero, the firmware environment variable is deleted.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error codes include ERROR_INVALID_FUNCTION.




## -remarks



Starting with Windows 10, version 1803, Universal Windows apps can read and write UEFI firmware variables. See <a href="https://msdn.microsoft.com/en-us/library/Mt829375(v=VS.85).aspx">Access UEFI firmware variables from a Universal Windows App</a>for details.

Starting with Windows 10, version 1803, reading UEFI firmware variables is also supported from User-Mode Driver Framework (UMDF) drivers. Writing UEFI firmware variables from UMDF drivers is not supported.

To write a firmware environment variable, the user account that the app is running under must have the <a href="https://msdn.microsoft.com/library/windows/desktop/bb530716(v=vs.85).aspx">SE_SYSTEM_ENVIRONMENT_NAME</a> privilege. A Universal Windows app must be run from an administrator account and follow the requirements outlined in <a href="https://msdn.microsoft.com/en-us/library/Mt829375(v=VS.85).aspx">Access UEFI firmware variables from a Universal Windows App</a>.

The exact set of firmware environment variables is determined by the boot firmware. The location of these environment variables is also specified by the firmware.  For example, on a UEFI-based system, NVRAM contains firmware environment variables that specify system boot settings. For information about specific variables used, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=183072">UEFI specification</a>. For more information about UEFI and Windows, see <a href="http://go.microsoft.com/fwlink/p/?linkid=183071">UEFI and Windows</a>.

Firmware variables are not supported on a legacy BIOS-based system. The <b>SetFirmwareEnvironmentVariable</b> function will always fail on a legacy BIOS-based system, or if Windows was installed using legacy BIOS on a system that supports both legacy BIOS and UEFI.  To identify these conditions, call the function with a dummy firmware environment name such as an empty string ("") for the <i>lpName</i> parameter and a dummy GUID such as "{00000000-0000-0000-0000-000000000000}" for the <i>lpGuid</i> parameter. On a legacy BIOS-based system, or on a system that supports both legacy BIOS and UEFI where Windows was installed using legacy BIOS, the function will fail with  ERROR_INVALID_FUNCTION. On a UEFI-based system, the function will  fail with an error specific to the firmware, such as ERROR_NOACCESS, to indicate that the dummy GUID namespace does not exist.

<b>SetFirmwareEnvironmentVariable</b> is the user-mode equivalent of the <a href="https://msdn.microsoft.com/04447D92-EB9E-400B-A018-E70B186EA3DB">ExSetFirmwareEnvironmentVariable</a> kernel-mode routine.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt829375(v=VS.85).aspx">Access UEFI firmware variables from a Universal Windows App</a>



<a href="https://msdn.microsoft.com/18e74e54-ecfe-46bf-8c9d-9eb16d22f3ba">GetFirmwareEnvironmentVariable</a>



<a href="https://msdn.microsoft.com/D3C2F03F-66F6-40A4-830E-058BBA925ACD">SetFirmwareEnvironmentVariableEx</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System
		  Information Functions</a>
 

 

