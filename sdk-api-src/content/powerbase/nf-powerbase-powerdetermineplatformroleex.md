---
UID: NF:powerbase.PowerDeterminePlatformRoleEx
title: PowerDeterminePlatformRoleEx function (powerbase.h)
description: Determines the computer role for the specified platform.
helpviewer_keywords: ["POWER_PLATFORM_ROLE_V1","POWER_PLATFORM_ROLE_V2","POWER_PLATFORM_ROLE_VERSION","PowerDeterminePlatformRoleEx","PowerDeterminePlatformRoleEx function","base.powerdetermineplatformroleex","powerbase/PowerDeterminePlatformRoleEx"]
old-location: base\powerdetermineplatformroleex.htm
tech.root: base
ms.assetid: 64b597d3-ca7a-4ff7-8527-72c3625147cd
ms.date: 12/05/2018
ms.keywords: POWER_PLATFORM_ROLE_V1, POWER_PLATFORM_ROLE_V2, POWER_PLATFORM_ROLE_VERSION, PowerDeterminePlatformRoleEx, PowerDeterminePlatformRoleEx function, base.powerdetermineplatformroleex, powerbase/PowerDeterminePlatformRoleEx
req.header: powerbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Powrprof.lib
req.dll: Powrprof.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerDeterminePlatformRoleEx
 - powerbase/PowerDeterminePlatformRoleEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Powrprof.dll
 - API-MS-Win-power-base-l1-1-0.dll
api_name:
 - PowerDeterminePlatformRoleEx
---

# PowerDeterminePlatformRoleEx function


## -description

Determines the computer role for the specified platform.

## -parameters

### -param Version [in]

The version of the <a href="/windows/desktop/api/winnt/ne-winnt-power_platform_role">POWER_PLATFORM_ROLE</a> enumeration for the platform. This parameter can be one of the following values.

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
The version of the <a href="/windows/desktop/api/winnt/ne-winnt-power_platform_role">POWER_PLATFORM_ROLE</a> enumeration for the current build target.

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_PLATFORM_ROLE_V1"></a><a id="power_platform_role_v1"></a><dl>
<dt><b>POWER_PLATFORM_ROLE_V1</b></dt>
</dl>
</td>
<td width="60%">
The version of the <a href="/windows/desktop/api/winnt/ne-winnt-power_platform_role">POWER_PLATFORM_ROLE</a> enumeration for Windows 7, Windows Server 2008 R2, Windows Vista or Windows Server 2008.

Calling <b>PowerDeterminePlatformRoleEx</b> with this value returns the same result as calling <a href="/windows/desktop/api/powrprof/nf-powrprof-powerdetermineplatformrole">PowerDeterminePlatformRole</a> on Windows 7, Windows Server 2008 R2, Windows Vista or Windows Server 2008. 

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_PLATFORM_ROLE_V2"></a><a id="power_platform_role_v2"></a><dl>
<dt><b>POWER_PLATFORM_ROLE_V2</b></dt>
</dl>
</td>
<td width="60%">
The version of the <a href="/windows/desktop/api/winnt/ne-winnt-power_platform_role">POWER_PLATFORM_ROLE</a> enumeration for Windows 8 and Windows Server 2012.

</td>
</tr>
</table>

## -returns

The return value is one of the values from the 
      specified version of the <a href="/windows/desktop/api/winnt/ne-winnt-power_platform_role">POWER_PLATFORM_ROLE</a> enumeration.

## -remarks

This function reads the ACPI Fixed ACPI Description Table (FADT) to determine the OEM preferred computer role. If that information is not available, the function looks for a battery. If at least one battery is available, the function returns <b>PlatformRoleMobile</b>. If no batteries are available, the function returns <b>PlatformRoleDesktop</b>.



If the OEM preferred computer role is not supported on the platform specified by the caller, the function returns the closest supported value.  For example, calling the <b>PowerDeterminePlatformRoleEx</b> function with a <i>Version</i> of <b>POWER_PLATFORM_ROLE_V1</b> on a tablet device returns <b>PlatformRoleMobile</b>.

## -see-also

<a href="/windows/desktop/api/winnt/ne-winnt-power_platform_role">POWER_PLATFORM_ROLE</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-powerdetermineplatformrole">PowerDeterminePlatformRole</a>