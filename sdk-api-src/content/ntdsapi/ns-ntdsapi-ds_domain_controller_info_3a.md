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

# DS_DOMAIN_CONTROLLER_INFO_3A structure


## -description


The <b>DS_DOMAIN_CONTROLLER_INFO_3</b> structure contains data about a domain controller. This structure is returned by the 
<a href="https://msdn.microsoft.com/52db3b25-e6b0-4a0d-831b-89a203580cf1">DsGetDomainControllerInfo</a> function.


## -struct-fields




### -field NetbiosName.string

 


### -field NetbiosName.unique

 


### -field DnsHostName.string

 


### -field DnsHostName.unique

 


### -field SiteName.string

 


### -field SiteName.unique

 


### -field SiteObjectName.string

 


### -field SiteObjectName.unique

 


### -field ComputerObjectName.string

 


### -field ComputerObjectName.unique

 


### -field ServerObjectName.string

 


### -field ServerObjectName.unique

 


### -field NtdsDsaObjectName.string

 


### -field NtdsDsaObjectName.unique

 


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
 

 

