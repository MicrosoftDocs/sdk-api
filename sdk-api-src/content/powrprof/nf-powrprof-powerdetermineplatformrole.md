---
UID: NF:powrprof.PowerDeterminePlatformRole
title: PowerDeterminePlatformRole function
author: windows-driver-content
description: Determines the computer role for Windows 7, Windows Server 2008 R2, Windows Vista or Windows Server 2008.
old-location: base\powerdetermineplatformrole.htm
old-project: Power
ms.assetid: a0311454-3908-49a6-95c0-c118dca259ac
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PowerDeterminePlatformRole, PowerDeterminePlatformRole function, base.powerdetermineplatformrole, powrprof/PowerDeterminePlatformRole
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: POWER_DATA_ACCESSOR, *PPOWER_DATA_ACCESSOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	PowrProf.dll
api_name:
-	PowerDeterminePlatformRole
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

