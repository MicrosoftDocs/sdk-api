---
UID: NE:winnt._POWER_PLATFORM_ROLE
title: POWER_PLATFORM_ROLE (winnt.h)
description: Indicates the OEM's preferred power management profile.
helpviewer_keywords: ["*PPOWER_PLATFORM_ROLE","POWER_PLATFORM_ROLE","POWER_PLATFORM_ROLE enumeration","PlatformRoleAppliancePC","PlatformRoleDesktop","PlatformRoleEnterpriseServer","PlatformRoleMaximum","PlatformRoleMobile","PlatformRolePerformanceServer","PlatformRoleSOHOServer","PlatformRoleSlate","PlatformRoleUnspecified","PlatformRoleWorkstation","base.power_platform_role","winnt/POWER_PLATFORM_ROLE","winnt/PlatformRoleAppliancePC","winnt/PlatformRoleDesktop","winnt/PlatformRoleEnterpriseServer","winnt/PlatformRoleMaximum","winnt/PlatformRoleMobile","winnt/PlatformRolePerformanceServer","winnt/PlatformRoleSOHOServer","winnt/PlatformRoleSlate","winnt/PlatformRoleUnspecified","winnt/PlatformRoleWorkstation"]
old-location: base\power_platform_role.htm
tech.root: base
ms.assetid: ec94a0c4-8451-47a5-be48-9d5ed76c3585
ms.date: 12/05/2018
ms.keywords: '*PPOWER_PLATFORM_ROLE, POWER_PLATFORM_ROLE, POWER_PLATFORM_ROLE enumeration, PlatformRoleAppliancePC, PlatformRoleDesktop, PlatformRoleEnterpriseServer, PlatformRoleMaximum, PlatformRoleMobile, PlatformRolePerformanceServer, PlatformRoleSOHOServer, PlatformRoleSlate, PlatformRoleUnspecified, PlatformRoleWorkstation, base.power_platform_role, winnt/POWER_PLATFORM_ROLE, winnt/PlatformRoleAppliancePC, winnt/PlatformRoleDesktop, winnt/PlatformRoleEnterpriseServer, winnt/PlatformRoleMaximum, winnt/PlatformRoleMobile, winnt/PlatformRolePerformanceServer, winnt/PlatformRoleSOHOServer, winnt/PlatformRoleSlate, winnt/PlatformRoleUnspecified, winnt/PlatformRoleWorkstation'
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: POWER_PLATFORM_ROLE, *PPOWER_PLATFORM_ROLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POWER_PLATFORM_ROLE
 - winnt/_POWER_PLATFORM_ROLE
 - PPOWER_PLATFORM_ROLE
 - winnt/PPOWER_PLATFORM_ROLE
 - POWER_PLATFORM_ROLE
 - winnt/POWER_PLATFORM_ROLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - POWER_PLATFORM_ROLE
---

# POWER_PLATFORM_ROLE enumeration


## -description

Indicates the OEM's preferred power management profile. These values are read from the 
    Preferred_PM_Profile field of the Fixed ACPI Description Table (FADT). These values are returned by the 
    <a href="/windows/desktop/api/powrprof/nf-powrprof-powerdetermineplatformrole">PowerDeterminePlatformRole</a> or <a href="/windows/desktop/api/powerbase/nf-powerbase-powerdetermineplatformroleex">PowerDeterminePlatformRoleEx </a>       function.

## -enum-fields

### -field PlatformRoleUnspecified:0

The OEM did not specify a specific role.

### -field PlatformRoleDesktop

The OEM specified a desktop role.

### -field PlatformRoleMobile

The OEM specified a mobile role (for example, a laptop).

### -field PlatformRoleWorkstation

The OEM specified a workstation role.

### -field PlatformRoleEnterpriseServer

The OEM specified an enterprise server role.

### -field PlatformRoleSOHOServer

The OEM specified a single office/home office (SOHO) server role.

### -field PlatformRoleAppliancePC

The OEM specified an appliance PC role.

### -field PlatformRolePerformanceServer

The OEM specified a performance server role.

### -field PlatformRoleSlate

The OEM specified a tablet form factor role.

<b>Windows 7, Windows Server 2008 R2, Windows Vista or Windows Server 2008:  </b>In version 1 of this enumeration, this value is equivalent to <b>PlatformRoleMaximum</b>. This value is supported in version 2 of this enumeration starting with Windows 8 and Windows Server 2012.

### -field PlatformRoleMaximum

Values equal to or greater than this value indicate an out of range value.

## -see-also

<a href="/windows/desktop/Power/power-management-enumeration-types">Power Management Enumeration Types</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-powerdetermineplatformrole">PowerDeterminePlatformRole</a>
