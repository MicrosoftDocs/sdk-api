---
UID: NS:ntdsapi.__unnamed_struct_18
title: DS_DOMAIN_CONTROLLER_INFO_3W
author: windows-sdk-content
description: The DS_DOMAIN_CONTROLLER_INFO_3 structure contains data about a domain controller. This structure is returned by the DsGetDomainControllerInfo function.
old-location: ad\ds_domain_controller_info_3.htm
tech.root: ad
ms.assetid: 510f458e-4c08-41c7-b290-1372ac9c8beb
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PDS_DOMAIN_CONTROLLER_INFO_3W, DS_DOMAIN_CONTROLLER_INFO_3, DS_DOMAIN_CONTROLLER_INFO_3 structure [Active Directory], DS_DOMAIN_CONTROLLER_INFO_3A, DS_DOMAIN_CONTROLLER_INFO_3W, PDS_DOMAIN_CONTROLLER_INFO_3, PDS_DOMAIN_CONTROLLER_INFO_3 structure pointer [Active Directory], ad.ds_domain_controller_info_3, ntdsapi/DS_DOMAIN_CONTROLLER_INFO_3, ntdsapi/DS_DOMAIN_CONTROLLER_INFO_3A, ntdsapi/DS_DOMAIN_CONTROLLER_INFO_3W, ntdsapi/PDS_DOMAIN_CONTROLLER_INFO_3"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DS_DOMAIN_CONTROLLER_INFO_3W (Unicode) and DS_DOMAIN_CONTROLLER_INFO_3A (ANSI)
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
 - Ntdsapi.h
api_name:
 - DS_DOMAIN_CONTROLLER_INFO_3
 - DS_DOMAIN_CONTROLLER_INFO_3A
 - DS_DOMAIN_CONTROLLER_INFO_3W
product: Windows
targetos: Windows
req.typenames: DS_DOMAIN_CONTROLLER_INFO_3W, *PDS_DOMAIN_CONTROLLER_INFO_3W
req.redist: 
---

# DS_DOMAIN_CONTROLLER_INFO_3W structure


## -description


The <b>DS_DOMAIN_CONTROLLER_INFO_3</b> structure contains data about a domain controller. This structure is returned by the 
<a href="https://msdn.microsoft.com/52db3b25-e6b0-4a0d-831b-89a203580cf1">DsGetDomainControllerInfo</a> function.


## -struct-fields




### -field string

 


### -field unique

 


### -field NetbiosName

Pointer to a null-terminated string that specifies the NetBIOS name of the domain controller.


### -field DnsHostName

Pointer to a null-terminated  string that specifies the DNS host name of the domain controller.


### -field SiteName

Pointer to a null-terminated  string that specifies the site to which the domain controller belongs.


### -field SiteObjectName

Pointer to a null-terminated  string that specifies the name of the site object on the domain controller.


### -field ComputerObjectName

Pointer to a null-terminated  string that specifies the name of the computer object on the domain controller.


### -field ServerObjectName

Pointer to a null-terminated  string that specifies the name of the server object on the domain controller.


### -field NtdsDsaObjectName

Pointer to a null-terminated  string that specifies the name of the NTDS DSA object on the domain controller.


### -field fIsPdc

A Boolean value that indicates whether or not this domain controller is the primary domain controller. If this value is <b>TRUE</b>, the domain controller is the primary domain controller; otherwise, the domain controller is not the primary domain controller.


### -field fDsEnabled

A Boolean value that indicates whether or not the domain controller is enabled. If this value is <b>TRUE</b>, the domain controller is enabled; otherwise, it is not enabled.


### -field fIsGc

A Boolean value that indicates whether or not the domain controller is global catalog server. If this value is <b>TRUE</b>, the domain controller is a global catalog server; otherwise, it is not a global catalog server.


### -field fIsRodc

A Boolean value that indicates if the domain controller is a read-only domain controller. If this value is <b>TRUE</b>, the domain controller is a read-only domain controller; otherwise, it is not a read-only domain controller.


### -field SiteObjectGuid

Contains the <b>GUID</b> for the site object on the domain controller.


### -field ComputerObjectGuid

Contains the <b>GUID</b> for the computer object on the domain controller.


### -field ServerObjectGuid

Contains the <b>GUID</b> for the server object on the domain controller.


### -field NtdsDsaObjectGuid

Contains the <b>GUID</b> for the NTDS DSA object on the domain controller.


## -remarks



The <a href="https://msdn.microsoft.com/52db3b25-e6b0-4a0d-831b-89a203580cf1">DsGetDomainControllerInfo</a> function can return different versions of this structure. For more information and a list of the currently supported versions, see the <i>InfoLevel</i> parameter of <b>DsGetDomainControllerInfo</b>.




## -see-also




<a href="https://msdn.microsoft.com/42b20d3b-1799-4f5f-b74e-fe9284dd8ac3">Domain Controller and Replication Management Structures</a>



<a href="https://msdn.microsoft.com/52db3b25-e6b0-4a0d-831b-89a203580cf1">DsGetDomainControllerInfo</a>
 

 

