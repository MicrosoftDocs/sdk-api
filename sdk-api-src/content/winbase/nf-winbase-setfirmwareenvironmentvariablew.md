---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SetFirmwareEnvironmentVariableW function


## -description


Sets the value of the specified firmware environment variable.


## -parameters




### -param lpName [in]

The name of the firmware environment variable. The pointer must not be <b>NULL</b>.


### -param lpGuid [in]

The GUID that represents the namespace of the firmware environment variable. The GUID must be a string in the format  "{<i>xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx</i>}". If the system does not support GUID-based namespaces, this parameter is ignored.


### -param pValue

TBD


### -param nSize [in]

The size of the <i>pBuffer</i> buffer, in bytes. If this parameter is zero, the firmware environment variable is deleted.


#### - pBuffer [in]

A pointer to the new value for the  firmware environment variable.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error codes include ERROR_INVALID_FUNCTION.




## -remarks



Starting with Windows 10, version 1803, Universal Windows apps can read and write UEFI firmware variables. See <a href="https://msdn.microsoft.com/4131CCED-3B76-4569-B0A7-111E4E9215EF">Access UEFI firmware variables from a Universal Windows App</a>
 for details.

Starting with Windows 10, version 1803, reading UEFI firmware variables is also supported from User-Mode Driver Framework (UMDF) drivers. Writing UEFI firmware variables from UMDF drivers is not supported.

To write a firmware environment variable, the user account that the app is running under must have the <a href="https://msdn.microsoft.com/library/windows/desktop/bb530716(v=vs.85).aspx">SE_SYSTEM_ENVIRONMENT_NAME</a> privilege. A Universal Windows app must be run from an administrator account and follow the requirements outlined in <a href="https://msdn.microsoft.com/4131CCED-3B76-4569-B0A7-111E4E9215EF">Access UEFI firmware variables from a Universal Windows App</a>
.

The exact set of firmware environment variables is determined by the boot firmware. The location of these environment variables is also specified by the firmware.  For example, on a UEFI-based system, NVRAM contains firmware environment variables that specify system boot settings. For information about specific variables used, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=183072">UEFI specification</a>. For more information about UEFI and Windows, see <a href="http://go.microsoft.com/fwlink/p/?linkid=183071">UEFI and Windows</a>.

Firmware variables are not supported on a legacy BIOS-based system. The <b>SetFirmwareEnvironmentVariable</b> function will always fail on a legacy BIOS-based system, or if Windows was installed using legacy BIOS on a system that supports both legacy BIOS and UEFI.  To identify these conditions, call the function with a dummy firmware environment name such as an empty string ("") for the <i>lpName</i> parameter and a dummy GUID such as "{00000000-0000-0000-0000-000000000000}" for the <i>lpGuid</i> parameter. On a legacy BIOS-based system, or on a system that supports both legacy BIOS and UEFI where Windows was installed using legacy BIOS, the function will fail with  ERROR_INVALID_FUNCTION. On a UEFI-based system, the function will  fail with an error specific to the firmware, such as ERROR_NOACCESS, to indicate that the dummy GUID namespace does not exist.

<b>SetFirmwareEnvironmentVariable</b> is the user-mode equivalent of the <a href="https://msdn.microsoft.com/library/windows/hardware/jj151554">ExSetFirmwareEnvironmentVariable</a> kernel-mode routine.




## -see-also




<a href="https://msdn.microsoft.com/4131CCED-3B76-4569-B0A7-111E4E9215EF">Access UEFI firmware variables from a Universal Windows App</a>



<a href="https://msdn.microsoft.com/18e74e54-ecfe-46bf-8c9d-9eb16d22f3ba">GetFirmwareEnvironmentVariable</a>



<a href="https://msdn.microsoft.com/D3C2F03F-66F6-40A4-830E-058BBA925ACD">SetFirmwareEnvironmentVariableEx</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System
		  Information Functions</a>
 

 

