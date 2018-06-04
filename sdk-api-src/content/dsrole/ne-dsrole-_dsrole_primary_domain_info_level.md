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

# _DSROLE_PRIMARY_DOMAIN_INFO_LEVEL enumeration


## -description


The <b>DSROLE_PRIMARY_DOMAIN_INFO_LEVEL</b> enumeration is used with the <a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a> function to specify the type of data to retrieve.


## -enum-fields




### -field DsRolePrimaryDomainInfoBasic

The <a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a> function retrieves data from a <a href="https://msdn.microsoft.com/8a7b34e8-46d6-46dc-9fef-ec37b0f65eea">DSROLE_PRIMARY_DOMAIN_INFO_BASIC</a> structure.


### -field DsRoleUpgradeStatus

The <a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a> function retrieves from a 
<a href="https://msdn.microsoft.com/c368d8d9-a91d-4013-880e-36a47d42a697">DSROLE_UPGRADE_STATUS_INFO</a> structure.


### -field DsRoleOperationState

The <a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a> function retrieves data from a 
<a href="https://msdn.microsoft.com/c6c8e510-190a-47ad-805c-b8d3fbee836d">DSROLE_OPERATION_STATE_INFO</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/c6c8e510-190a-47ad-805c-b8d3fbee836d">DSROLE_OPERATION_STATE_INFO</a>



<a href="https://msdn.microsoft.com/8a7b34e8-46d6-46dc-9fef-ec37b0f65eea">DSROLE_PRIMARY_DOMAIN_INFO_BASIC</a>



<a href="https://msdn.microsoft.com/c368d8d9-a91d-4013-880e-36a47d42a697">DSROLE_UPGRADE_STATUS_INFO</a>



<a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

