---
UID: NS:dsrole._DSROLE_PRIMARY_DOMAIN_INFO_BASIC
title: "_DSROLE_PRIMARY_DOMAIN_INFO_BASIC"
author: windows-sdk-content
description: Used with the DsRoleGetPrimaryDomainInformation function to contain domain data.
old-location: ad\dsrole_primary_domain_info_basic.htm
tech.root: ad
ms.assetid: 8a7b34e8-46d6-46dc-9fef-ec37b0f65eea
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PDSROLE_PRIMARY_DOMAIN_INFO_BASIC, DSROLE_PRIMARY_DOMAIN_GUID_PRESENT, DSROLE_PRIMARY_DOMAIN_INFO_BASIC, DSROLE_PRIMARY_DOMAIN_INFO_BASIC structure [Active Directory], DSROLE_PRIMARY_DS_MIXED_MODE, DSROLE_PRIMARY_DS_READONLY, DSROLE_PRIMARY_DS_RUNNING, DSROLE_UPGRADE_IN_PROGRESS, PDSROLE_PRIMARY_DOMAIN_INFO_BASIC, PDSROLE_PRIMARY_DOMAIN_INFO_BASIC structure pointer [Active Directory], _DSROLE_PRIMARY_DOMAIN_INFO_BASIC, _glines_dsrole_primary_domain_info_basic, ad.dsrole__primary__domain__info__basic, ad.dsrole_primary_domain_info_basic, dsrole/DSROLE_PRIMARY_DOMAIN_INFO_BASIC, dsrole/PDSROLE_PRIMARY_DOMAIN_INFO_BASIC"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - DSROLE_PRIMARY_DOMAIN_INFO_BASIC
product: Windows
targetos: Windows
req.typenames: DSROLE_PRIMARY_DOMAIN_INFO_BASIC, *PDSROLE_PRIMARY_DOMAIN_INFO_BASIC
req.redist: 
---

# _DSROLE_PRIMARY_DOMAIN_INFO_BASIC structure


## -description


The <b>DSROLE_PRIMARY_DOMAIN_INFO_BASIC</b> structure is used with the <a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a> function to contain domain  data.


## -struct-fields




### -field MachineRole

Contains one of the <a href="https://msdn.microsoft.com/d5255070-71dd-4510-8bec-a84726a241c6">DSROLE_MACHINE_ROLE</a> values that specifies the role of the computer.


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




<a href="https://msdn.microsoft.com/d5255070-71dd-4510-8bec-a84726a241c6">DSROLE_MACHINE_ROLE</a>



<a href="https://msdn.microsoft.com/4df5f356-a39b-40a4-9e62-994ad27df3a9">Directory Service Structures</a>



<a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a>
 

 

