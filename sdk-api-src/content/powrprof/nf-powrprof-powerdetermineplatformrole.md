---
UID: NF:powrprof.PowerDeterminePlatformRole
title: PowerDeterminePlatformRole function (powrprof.h)
description: Determines the computer role for Windows 7, Windows Server 2008 R2, Windows Vista or Windows Server 2008.
old-location: base\powerdetermineplatformrole.htm
tech.root: power
ms.assetid: a0311454-3908-49a6-95c0-c118dca259ac
ms.date: 12/05/2018
ms.keywords: PowerDeterminePlatformRole, PowerDeterminePlatformRole function, base.powerdetermineplatformrole, powrprof/PowerDeterminePlatformRole
ms.topic: function
f1_keywords:
- powrprof/PowerDeterminePlatformRole
dev_langs:
- c++
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
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- PowrProf.dll
api_name:
- PowerDeterminePlatformRole
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PowerDeterminePlatformRole function


## -description


Determines the computer role for Windows 7, Windows Server 2008 R2, Windows Vista or Windows Server 2008. To specify a different platform, use the <a href="https://docs.microsoft.com/windows/desktop/api/powerbase/nf-powerbase-powerdetermineplatformroleex">PowerDeterminePlatformRoleEx</a> function. 

To query additional power platform roles defined after Windows 7 and Windows Server 2008 R2, use <a href="https://docs.microsoft.com/windows/desktop/api/powerbase/nf-powerbase-powerdetermineplatformroleex">PowerDeterminePlatformRoleEx</a>. 


## -parameters






## -returns



The return value is one of the values from the 
      <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-power_platform_role">POWER_PLATFORM_ROLE</a> enumeration.




## -remarks



This function reads the ACPI Fixed ACPI Description Table (FADT) to determine the OEM preferred computer role. If that information is not available, the function looks for a battery. If at least one battery is available, the function returns <b>PlatformRoleMobile</b>. If no batteries are available, the function returns <b>PlatformRoleDesktop</b>.



<div class="alert"><b>Note</b>  This API has a newer version. To query additional power platform roles defined after Windows 7 and Windows Server 2008 R2, use <a href="https://docs.microsoft.com/windows/desktop/api/powerbase/nf-powerbase-powerdetermineplatformroleex">PowerDeterminePlatformRoleEx</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-power_platform_role">POWER_PLATFORM_ROLE</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powerbase/nf-powerbase-powerdetermineplatformroleex">PowerDeterminePlatformRoleEx</a>
 

 

