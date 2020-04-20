---
UID: NF:ntdsapi.DsListRolesA
title: DsListRolesA function (ntdsapi.h)
description: The DsListRoles function lists roles recognized by the server.helpviewer_keywords: ["DS_ROLE_DOMAIN_OWNER","DS_ROLE_INFRASTRUCTURE_OWNER","DS_ROLE_PDC_OWNER","DS_ROLE_RID_OWNER","DS_ROLE_SCHEMA_OWNER","DsListRoles","DsListRoles function [Active Directory]","DsListRolesA","DsListRolesW","_glines_dslistroles","ad.dslistroles","ntdsapi/DsListRoles","ntdsapi/DsListRolesA","ntdsapi/DsListRolesW"]
old-location: ad\dslistroles.htm
tech.root: ad
ms.assetid: 679a2dca-019b-4f6e-acd9-efb30e0d4b44
ms.date: 12/05/2018
ms.keywords: DS_ROLE_DOMAIN_OWNER, DS_ROLE_INFRASTRUCTURE_OWNER, DS_ROLE_PDC_OWNER, DS_ROLE_RID_OWNER, DS_ROLE_SCHEMA_OWNER, DsListRoles, DsListRoles function [Active Directory], DsListRolesA, DsListRolesW, _glines_dslistroles, ad.dslistroles, ntdsapi/DsListRoles, ntdsapi/DsListRolesA, ntdsapi/DsListRolesW
f1_keywords:
- ntdsapi/DsListRoles
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsListRolesA function


## -description


The <b>DsListRoles</b> function lists roles recognized by the server.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.


### -param ppRoles [out]

Pointer to a variable that receives a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure containing the roles the server recognizes. The returned structure must be deallocated using 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>.

The indexes of the array in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure indicate what data are contained by each array element. The following constants may be used to specify the desired index for a particular piece of data.



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


## -returns



If the function returns a list of roles, the return value is <b>NO_ERROR</b>.

If the function fails, the return value can be one of the following error codes.

Individual name conversion errors are reported in the returned <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>
 

 

