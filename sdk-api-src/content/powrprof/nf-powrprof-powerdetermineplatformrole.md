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

# PowerDeterminePlatformRole function


## -description


Determines the computer role for Windows 7, Windows Server 2008 R2, Windows Vista or Windows Server 2008. To specify a different platform, use the <a href="https://msdn.microsoft.com/64b597d3-ca7a-4ff7-8527-72c3625147cd">PowerDeterminePlatformRoleEx</a> function. 

To query additional power platform roles defined after Windows 7 and Windows Server 2008 R2, use <a href="https://msdn.microsoft.com/64b597d3-ca7a-4ff7-8527-72c3625147cd">PowerDeterminePlatformRoleEx</a>. 


## -parameters






## -returns



The return value is one of the values from the 
      <a href="https://msdn.microsoft.com/ec94a0c4-8451-47a5-be48-9d5ed76c3585">POWER_PLATFORM_ROLE</a> enumeration.




## -remarks



This function reads the ACPI Fixed ACPI Description Table (FADT) to determine the OEM preferred computer role. If that information is not available, the function looks for a battery. If at least one battery is available, the function returns <b>PlatformRoleMobile</b>. If no batteries are available, the function returns <b>PlatformRoleDesktop</b>.



<div class="alert"><b>Note</b>  This API has a newer version. To query additional power platform roles defined after Windows 7 and Windows Server 2008 R2, use <a href="https://msdn.microsoft.com/64b597d3-ca7a-4ff7-8527-72c3625147cd">PowerDeterminePlatformRoleEx</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ec94a0c4-8451-47a5-be48-9d5ed76c3585">POWER_PLATFORM_ROLE</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/64b597d3-ca7a-4ff7-8527-72c3625147cd">PowerDeterminePlatformRoleEx</a>
 

 

