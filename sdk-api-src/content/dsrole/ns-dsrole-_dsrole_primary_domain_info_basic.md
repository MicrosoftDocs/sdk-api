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
 

 

