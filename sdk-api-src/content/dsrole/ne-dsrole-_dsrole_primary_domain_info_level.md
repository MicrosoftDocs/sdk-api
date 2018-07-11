---
UID: NE:dsrole._DSROLE_PRIMARY_DOMAIN_INFO_LEVEL
title: "_DSROLE_PRIMARY_DOMAIN_INFO_LEVEL"
author: windows-sdk-content
description: Used with the DsRoleGetPrimaryDomainInformation function to specify the type of data to retrieve.
old-location: ad\dsrole_primary_domain_info_level.htm
old-project: ad
ms.assetid: c8b141b1-d5fa-4ec9-8899-a1b0f6a4ce1d
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: DSROLE_PRIMARY_DOMAIN_INFO_LEVEL, DSROLE_PRIMARY_DOMAIN_INFO_LEVEL enumeration [Active Directory], DsRoleOperationState, DsRolePrimaryDomainInfoBasic, DsRoleUpgradeStatus, _DSROLE_PRIMARY_DOMAIN_INFO_LEVEL, ad.dsrole_primary_domain_info_level, dsrole/DSROLE_PRIMARY_DOMAIN_INFO_LEVEL, dsrole/DsRoleOperationState, dsrole/DsRolePrimaryDomainInfoBasic, dsrole/DsRoleUpgradeStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dsrole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: DSROLE_PRIMARY_DOMAIN_INFO_LEVEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsrole.h
api_name:
 - DSROLE_PRIMARY_DOMAIN_INFO_LEVEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

