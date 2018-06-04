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

# _DSROLE_MACHINE_ROLE enumeration


## -description


The <b>DSROLE_MACHINE_ROLE</b> enumeration is used with the <b>MachineRole</b> member of the <a href="https://msdn.microsoft.com/8a7b34e8-46d6-46dc-9fef-ec37b0f65eea">DSROLE_PRIMARY_DOMAIN_INFO_BASIC</a> structure to specify the computer role.


## -enum-fields




### -field DsRole_RoleStandaloneWorkstation

The computer is a workstation that is not a member of a domain.


### -field DsRole_RoleMemberWorkstation

The computer is a workstation that is a member of a domain.


### -field DsRole_RoleStandaloneServer

The computer is a server that is not a member of a domain.


### -field DsRole_RoleMemberServer

The computer is a server that is a member of a domain.


### -field DsRole_RoleBackupDomainController

The computer is a backup domain controller.


### -field DsRole_RolePrimaryDomainController

The computer is a primary domain controller.


## -see-also




<a href="https://msdn.microsoft.com/8a7b34e8-46d6-46dc-9fef-ec37b0f65eea">DSROLE_PRIMARY_DOMAIN_INFO_BASIC</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

