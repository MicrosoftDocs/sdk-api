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

# PowerDeterminePlatformRoleEx function


## -description


Determines the computer role for the specified platform.


## -parameters




### -param Version [in]

The version of the <a href="https://msdn.microsoft.com/ec94a0c4-8451-47a5-be48-9d5ed76c3585">POWER_PLATFORM_ROLE</a> enumeration for the platform. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="POWER_PLATFORM_ROLE_VERSION"></a><a id="power_platform_role_version"></a><dl>
<dt><b>POWER_PLATFORM_ROLE_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The version of the <a href="https://msdn.microsoft.com/ec94a0c4-8451-47a5-be48-9d5ed76c3585">POWER_PLATFORM_ROLE</a> enumeration for the current build target.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_PLATFORM_ROLE_V1"></a><a id="power_platform_role_v1"></a><dl>
<dt><b>POWER_PLATFORM_ROLE_V1</b></dt>
</dl>
</td>
<td width="60%">
The version of the <a href="https://msdn.microsoft.com/ec94a0c4-8451-47a5-be48-9d5ed76c3585">POWER_PLATFORM_ROLE</a> enumeration for Windows 7, Windows Server 2008 R2, Windows Vista or Windows Server 2008.

Calling <b>PowerDeterminePlatformRoleEx</b> with this value returns the same result as calling <a href="https://msdn.microsoft.com/a0311454-3908-49a6-95c0-c118dca259ac">PowerDeterminePlatformRole</a> on Windows 7, Windows Server 2008 R2, Windows Vista or Windows Server 2008. 

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_PLATFORM_ROLE_V2"></a><a id="power_platform_role_v2"></a><dl>
<dt><b>POWER_PLATFORM_ROLE_V2</b></dt>
</dl>
</td>
<td width="60%">
The version of the <a href="https://msdn.microsoft.com/ec94a0c4-8451-47a5-be48-9d5ed76c3585">POWER_PLATFORM_ROLE</a> enumeration for Windows 8 and Windows Server 2012.

</td>
</tr>
</table>
 


## -returns



The return value is one of the values from the 
      specified version of the <a href="https://msdn.microsoft.com/ec94a0c4-8451-47a5-be48-9d5ed76c3585">POWER_PLATFORM_ROLE</a> enumeration.




## -remarks



This function reads the ACPI Fixed ACPI Description Table (FADT) to determine the OEM preferred computer role. If that information is not available, the function looks for a battery. If at least one battery is available, the function returns <b>PlatformRoleMobile</b>. If no batteries are available, the function returns <b>PlatformRoleDesktop</b>.



If the OEM preferred computer role is not supported on the platform specified by the caller, the function returns the closest supported value.  For example, calling the <b>PowerDeterminePlatformRoleEx</b> function with a <i>Version</i> of <b>POWER_PLATFORM_ROLE_V1</b> on a tablet device returns <b>PlatformRoleMobile</b>.  





## -see-also




<a href="https://msdn.microsoft.com/ec94a0c4-8451-47a5-be48-9d5ed76c3585">POWER_PLATFORM_ROLE</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/a0311454-3908-49a6-95c0-c118dca259ac">PowerDeterminePlatformRole</a>
 

 

