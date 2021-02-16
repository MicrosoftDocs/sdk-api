---
UID: NS:dsrole._DSROLE_PRIMARY_DOMAIN_INFO_BASIC
title: DSROLE_PRIMARY_DOMAIN_INFO_BASIC (dsrole.h)
description: Used with the DsRoleGetPrimaryDomainInformation function to contain domain data.
helpviewer_keywords: ["*PDSROLE_PRIMARY_DOMAIN_INFO_BASIC","DSROLE_PRIMARY_DOMAIN_GUID_PRESENT","DSROLE_PRIMARY_DOMAIN_INFO_BASIC","DSROLE_PRIMARY_DOMAIN_INFO_BASIC structure [Active Directory]","DSROLE_PRIMARY_DS_MIXED_MODE","DSROLE_PRIMARY_DS_READONLY","DSROLE_PRIMARY_DS_RUNNING","DSROLE_UPGRADE_IN_PROGRESS","PDSROLE_PRIMARY_DOMAIN_INFO_BASIC","PDSROLE_PRIMARY_DOMAIN_INFO_BASIC structure pointer [Active Directory]","_glines_dsrole_primary_domain_info_basic","ad.dsrole__primary__domain__info__basic","ad.dsrole_primary_domain_info_basic","dsrole/DSROLE_PRIMARY_DOMAIN_INFO_BASIC","dsrole/PDSROLE_PRIMARY_DOMAIN_INFO_BASIC"]
old-location: ad\dsrole_primary_domain_info_basic.htm
tech.root: ad
ms.assetid: 8a7b34e8-46d6-46dc-9fef-ec37b0f65eea
ms.date: 12/05/2018
ms.keywords: '*PDSROLE_PRIMARY_DOMAIN_INFO_BASIC, DSROLE_PRIMARY_DOMAIN_GUID_PRESENT, DSROLE_PRIMARY_DOMAIN_INFO_BASIC, DSROLE_PRIMARY_DOMAIN_INFO_BASIC structure [Active Directory], DSROLE_PRIMARY_DS_MIXED_MODE, DSROLE_PRIMARY_DS_READONLY, DSROLE_PRIMARY_DS_RUNNING, DSROLE_UPGRADE_IN_PROGRESS, PDSROLE_PRIMARY_DOMAIN_INFO_BASIC, PDSROLE_PRIMARY_DOMAIN_INFO_BASIC structure pointer [Active Directory], _glines_dsrole_primary_domain_info_basic, ad.dsrole__primary__domain__info__basic, ad.dsrole_primary_domain_info_basic, dsrole/DSROLE_PRIMARY_DOMAIN_INFO_BASIC, dsrole/PDSROLE_PRIMARY_DOMAIN_INFO_BASIC'
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
targetos: Windows
req.typenames: DSROLE_PRIMARY_DOMAIN_INFO_BASIC, *PDSROLE_PRIMARY_DOMAIN_INFO_BASIC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSROLE_PRIMARY_DOMAIN_INFO_BASIC
 - dsrole/_DSROLE_PRIMARY_DOMAIN_INFO_BASIC
 - PDSROLE_PRIMARY_DOMAIN_INFO_BASIC
 - dsrole/PDSROLE_PRIMARY_DOMAIN_INFO_BASIC
 - DSROLE_PRIMARY_DOMAIN_INFO_BASIC
 - dsrole/DSROLE_PRIMARY_DOMAIN_INFO_BASIC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsrole.h
api_name:
 - DSROLE_PRIMARY_DOMAIN_INFO_BASIC
---

# DSROLE_PRIMARY_DOMAIN_INFO_BASIC structure


## -description

The <b>DSROLE_PRIMARY_DOMAIN_INFO_BASIC</b> structure is used with the <a href="/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a> function to contain domain  data.

## -struct-fields

### -field MachineRole

Contains one of the <a href="/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role">DSROLE_MACHINE_ROLE</a> values that specifies the role of the computer.

### -field Flags

Contains a set of flags that provide additional domain data. This  can be a combination of one or more of the following values.



#### DSROLE_PRIMARY_DOMAIN_GUID_PRESENT

The <b>DomainGuid</b> member contains a valid domain <b>GUID</b>.



#### DSROLE_PRIMARY_DS_MIXED_MODE

The directory service is running in mixed mode. This flag is valid only if the <b>DSROLE_PRIMARY_DS_RUNNING</b> flag is set.



#### DSROLE_PRIMARY_DS_RUNNING

The directory service is running on this computer.



#### DSROLE_PRIMARY_DS_READONLY

The directory service is running as read-only on this computer.



#### DSROLE_UPGRADE_IN_PROGRESS

The computer is being upgraded from a previous version of Windows NT/Windows 2000.

### -field DomainNameFlat

Pointer to a null-terminated Unicode string that contains the NetBIOS domain name.

### -field DomainNameDns

Pointer to a null-terminated Unicode string that contains the DNS domain name. This member is optional and may be <b>NULL</b>.

### -field DomainForestName

Pointer to a null-terminated Unicode string that contains the forest name. This member is optional and may be <b>NULL</b>.

### -field DomainGuid

Contains the domain identifier. This member is valid only if the <b>Flags</b> member contains the <b>DSROLE_PRIMARY_DOMAIN_GUID_PRESENT</b> flag.

## -see-also

<a href="/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role">DSROLE_MACHINE_ROLE</a>



<a href="/windows/desktop/AD/directory-service-structures">Directory Service Structures</a>



<a href="/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a>