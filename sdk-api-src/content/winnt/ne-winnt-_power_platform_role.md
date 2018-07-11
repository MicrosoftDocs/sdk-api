---
UID: NE:winnt._POWER_PLATFORM_ROLE
title: "_POWER_PLATFORM_ROLE"
author: windows-sdk-content
description: Indicates the OEM's preferred power management profile.
old-location: base\power_platform_role.htm
old-project: power
ms.assetid: ec94a0c4-8451-47a5-be48-9d5ed76c3585
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: "*PPOWER_PLATFORM_ROLE, POWER_PLATFORM_ROLE, POWER_PLATFORM_ROLE enumeration, PlatformRoleAppliancePC, PlatformRoleDesktop, PlatformRoleEnterpriseServer, PlatformRoleMaximum, PlatformRoleMobile, PlatformRolePerformanceServer, PlatformRoleSOHOServer, PlatformRoleSlate, PlatformRoleUnspecified, PlatformRoleWorkstation, _POWER_PLATFORM_ROLE, base.power_platform_role, winnt/POWER_PLATFORM_ROLE, winnt/PlatformRoleAppliancePC, winnt/PlatformRoleDesktop, winnt/PlatformRoleEnterpriseServer, winnt/PlatformRoleMaximum, winnt/PlatformRoleMobile, winnt/PlatformRolePerformanceServer, winnt/PlatformRoleSOHOServer, winnt/PlatformRoleSlate, winnt/PlatformRoleUnspecified, winnt/PlatformRoleWorkstation"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: POWER_PLATFORM_ROLE, *PPOWER_PLATFORM_ROLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - POWER_PLATFORM_ROLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _POWER_PLATFORM_ROLE enumeration


## -description


Indicates the OEM's preferred power management profile. These values are read from the 
    Preferred_PM_Profile field of the Fixed ACPI Description Table (FADT). These values are returned by the 
    <a href="https://msdn.microsoft.com/a0311454-3908-49a6-95c0-c118dca259ac">PowerDeterminePlatformRole</a> or <a href="https://msdn.microsoft.com/64b597d3-ca7a-4ff7-8527-72c3625147cd">PowerDeterminePlatformRoleEx </a>       function.


## -enum-fields




### -field PlatformRoleUnspecified

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




<a href="https://msdn.microsoft.com/f78cd97f-586f-4091-ab4a-5f109a0f679a">Power Management Enumeration Types</a>



<a href="https://msdn.microsoft.com/a0311454-3908-49a6-95c0-c118dca259ac">PowerDeterminePlatformRole</a>
 

 

