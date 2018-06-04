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

# GetFirmwareEnvironmentVariableExW function


## -description


Retrieves the value of the specified firmware environment variable and its attributes.


## -parameters




### -param lpName

The name of the firmware environment variable. The pointer must not be <b>NULL</b>.


### -param lpGuid

The GUID that represents the namespace of the firmware environment variable. The GUID must be  a string in the format  "{<i>xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx</i>}" where 'x' represents a hexadecimal value. The pointer must not be <b>NULL</b>.


### -param pBuffer

TBD


### -param nSize

The size of the <i>pValue</i> buffer, in bytes.


### -param pdwAttribubutes

TBD




#### - pValue

A pointer to a buffer that receives the value of the specified firmware environment variable.


#### - pdwAttributes

Bitmask identifying UEFI variable attributes associated with the variable. See <a href="https://msdn.microsoft.com/D3C2F03F-66F6-40A4-830E-058BBA925ACD">SetFirmwareEnvironmentVariableEx</a> for the bitmask definition.


## -returns



If the function succeeds, the return value is the number of bytes stored in the <i>pValue</i> buffer.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error codes include ERROR_INVALID_FUNCTION.




## -remarks



Starting with Windows 10, version 1803, Universal Windows apps can read and write UEFI firmware variables. See <a href="https://msdn.microsoft.com/4131CCED-3B76-4569-B0A7-111E4E9215EF">Access UEFI firmware variables from a Universal Windows App</a>
 for details.

To read a UEFI firmware environment variable, the user account that the app is running under must have the <a href="https://msdn.microsoft.com/library/windows/desktop/bb530716(v=vs.85).aspx">SE_SYSTEM_ENVIRONMENT_NAME</a> privilege. A Universal Windows app must be run from an administrator account and follow the requirements outlined in <a href="https://msdn.microsoft.com/4131CCED-3B76-4569-B0A7-111E4E9215EF">Access UEFI firmware variables from a Universal Windows App</a>
.

Starting with Windows 10, version 1803, reading Unified Extensible Firmware Interface (UEFI) variables is also supported from User-Mode Driver Framework (UMDF) drivers. Writing UEFI variables from UMDF drivers is not supported.

The exact set of firmware environment variables is determined by the boot firmware. The location of these environment variables is also specified by the firmware.  For example, on a UEFI-based system, NVRAM contains firmware environment variables that specify system boot settings. For information about specific variables used, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=183072">UEFI specification</a>. For more information about UEFI and Windows, see <a href="http://go.microsoft.com/fwlink/p/?linkid=183071">UEFI and Windows</a>.

Firmware variables are not supported on a legacy BIOS-based system. The <b>GetFirmwareEnvironmentVariableEx</b> function will always fail on a legacy BIOS-based system, or if Windows was installed using legacy BIOS on a system that supports both legacy BIOS and UEFI. To identify these conditions, call the function with a dummy firmware environment name such as an empty string ("") for the <i>lpName</i> parameter and a dummy GUID such as "{00000000-0000-0000-0000-000000000000}" for the <i>lpGuid</i> parameter. On a legacy BIOS-based system, or on a system that supports both legacy BIOS and UEFI where Windows was installed using legacy BIOS, the function will fail with  ERROR_INVALID_FUNCTION. On a UEFI-based system, the function will  fail with an error specific to the firmware, such as ERROR_NOACCESS, to indicate that the dummy GUID namespace does not exist. 

If you are creating a backup application, you can use this function to save all the boot settings for the system so they can be restored using the <a href="https://msdn.microsoft.com/42117632-61aa-4f83-abe1-c08f40cf3f0a">SetFirmwareEnvironmentVariable</a> 
	 function if needed. 




## -see-also




<a href="https://msdn.microsoft.com/4131CCED-3B76-4569-B0A7-111E4E9215EF">Access UEFI firmware variables from a Universal Windows App</a>



<a href="https://msdn.microsoft.com/18e74e54-ecfe-46bf-8c9d-9eb16d22f3ba">GetFirmwareEnvironmentVariable</a>



<a href="https://msdn.microsoft.com/D3C2F03F-66F6-40A4-830E-058BBA925ACD">SetFirmwareEnvironmentVariableEx</a>
 

 

