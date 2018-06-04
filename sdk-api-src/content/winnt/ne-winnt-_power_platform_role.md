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
 

 

