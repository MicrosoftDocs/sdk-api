---
UID: NE:dsrole._DSROLE_PRIMARY_DOMAIN_INFO_LEVEL
title: DSROLE_PRIMARY_DOMAIN_INFO_LEVEL (dsrole.h)
author: windows-sdk-content
description: Used with the DsRoleGetPrimaryDomainInformation function to specify the type of data to retrieve.
old-location: ad\dsrole_primary_domain_info_level.htm
tech.root: ad
ms.assetid: c8b141b1-d5fa-4ec9-8899-a1b0f6a4ce1d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DSROLE_PRIMARY_DOMAIN_INFO_LEVEL, DSROLE_PRIMARY_DOMAIN_INFO_LEVEL enumeration [Active Directory], DsRoleOperationState, DsRolePrimaryDomainInfoBasic, DsRoleUpgradeStatus, ad.dsrole_primary_domain_info_level, dsrole/DSROLE_PRIMARY_DOMAIN_INFO_LEVEL, dsrole/DsRoleOperationState, dsrole/DsRolePrimaryDomainInfoBasic, dsrole/DsRoleUpgradeStatus
ms.topic: enum
f1_keywords: ["dsrole/DSROLE_PRIMARY_DOMAIN_INFO_LEVEL"]
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: DSROLE_PRIMARY_DOMAIN_INFO_LEVEL
req.redist: 
ms.custom: 19H1
---

# DSROLE_PRIMARY_DOMAIN_INFO_LEVEL enumeration


## -description


The <b>DSROLE_PRIMARY_DOMAIN_INFO_LEVEL</b> enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a> function to specify the type of data to retrieve.


## -enum-fields




### -field DsRolePrimaryDomainInfoBasic

The <a href="https://docs.microsoft.com/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a> function retrieves data from a <a href="https://docs.microsoft.com/windows/desktop/api/dsrole/ns-dsrole-_dsrole_primary_domain_info_basic">DSROLE_PRIMARY_DOMAIN_INFO_BASIC</a> structure.


### -field DsRoleUpgradeStatus

The <a href="https://docs.microsoft.com/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a> function retrieves from a 
<a href="https://docs.microsoft.com/windows/desktop/api/dsrole/ns-dsrole-_dsrole_upgrade_status_info">DSROLE_UPGRADE_STATUS_INFO</a> structure.


### -field DsRoleOperationState

The <a href="https://docs.microsoft.com/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a> function retrieves data from a 
<a href="https://docs.microsoft.com/windows/desktop/api/dsrole/ns-dsrole-_dsrole_operation_state_info">DSROLE_OPERATION_STATE_INFO</a> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dsrole/ns-dsrole-_dsrole_operation_state_info">DSROLE_OPERATION_STATE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsrole/ns-dsrole-_dsrole_primary_domain_info_basic">DSROLE_PRIMARY_DOMAIN_INFO_BASIC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsrole/ns-dsrole-_dsrole_upgrade_status_info">DSROLE_UPGRADE_STATUS_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>
 

 

