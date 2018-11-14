---
UID: NF:ntdsapi.DsListRolesW
title: DsListRolesW function
author: windows-sdk-content
description: The DsListRoles function lists roles recognized by the server.
old-location: ad\dslistroles.htm
tech.root: ad
ms.assetid: 679a2dca-019b-4f6e-acd9-efb30e0d4b44
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DS_ROLE_DOMAIN_OWNER, DS_ROLE_INFRASTRUCTURE_OWNER, DS_ROLE_PDC_OWNER, DS_ROLE_RID_OWNER, DS_ROLE_SCHEMA_OWNER, DsListRoles, DsListRoles function [Active Directory], DsListRolesA, DsListRolesW, _glines_dslistroles, ad.dslistroles, ntdsapi/DsListRoles, ntdsapi/DsListRolesA, ntdsapi/DsListRolesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsListRolesW (Unicode) and DsListRolesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsListRoles
 - DsListRolesA
 - DsListRolesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DsListRolesW
: 
---

# DsListRolesW function


## -description


The <b>DsListRoles</b> function lists roles recognized by the server.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param ppRoles [out]

Pointer to a variable that receives a pointer to a 
<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure containing the roles the server recognizes. The returned structure must be deallocated using 
<a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a>.

The indexes of the array in the <a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure indicate what data are contained by each array element. The following constants may be used to specify the desired index for a particular piece of data.



#### DS_ROLE_DOMAIN_OWNER

Server owns the domain.



#### DS_ROLE_INFRASTRUCTURE_OWNER

Server owns the infrastructure.



#### DS_ROLE_PDC_OWNER

Server owns the PDC.



#### DS_ROLE_RID_OWNER

Server owns the RID.



#### DS_ROLE_SCHEMA_OWNER

Server owns the schema.


##### - ppRoles.DS_ROLE_DOMAIN_OWNER

Server owns the domain.


##### - ppRoles.DS_ROLE_INFRASTRUCTURE_OWNER

Server owns the infrastructure.


##### - ppRoles.DS_ROLE_PDC_OWNER

Server owns the PDC.


##### - ppRoles.DS_ROLE_RID_OWNER

Server owns the RID.


##### - ppRoles.DS_ROLE_SCHEMA_OWNER

Server owns the schema.


## -returns



If the function returns a list of roles, the return value is <b>NO_ERROR</b>.

If the function fails, the return value can be one of the following error codes.

Individual name conversion errors are reported in the returned <a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a>
 

 

