---
UID: NF:dsrole.DsRoleGetPrimaryDomainInformation
title: DsRoleGetPrimaryDomainInformation function (dsrole.h)
description: Retrieves state data for the computer.
helpviewer_keywords: ["DsRoleGetPrimaryDomainInformation","DsRoleGetPrimaryDomainInformation function [Active Directory]","_glines_dsrolegetprimarydomaininformation","ad.dsrolegetprimarydomaininformation","dsrole/DsRoleGetPrimaryDomainInformation"]
old-location: ad\dsrolegetprimarydomaininformation.htm
tech.root: ad
ms.assetid: d54876e3-a622-4b44-a597-db0f710f7758
ms.date: 12/05/2018
ms.keywords: DsRoleGetPrimaryDomainInformation, DsRoleGetPrimaryDomainInformation function [Active Directory], _glines_dsrolegetprimarydomaininformation, ad.dsrolegetprimarydomaininformation, dsrole/DsRoleGetPrimaryDomainInformation
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsRoleGetPrimaryDomainInformation
 - dsrole/DsRoleGetPrimaryDomainInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - DsRoleGetPrimaryDomainInformation
---

# DsRoleGetPrimaryDomainInformation function


## -description

The <b>DsRoleGetPrimaryDomainInformation</b> function retrieves state data for the computer. This data includes the state of the directory service installation and domain data.

## -parameters

### -param lpServer [in]

Pointer to null-terminated Unicode string that contains the name of the computer on which to call the function. If this parameter is <b>NULL</b>, the local computer is used.

### -param InfoLevel [in]

Contains one of the <a href="/windows/desktop/api/dsrole/ne-dsrole-dsrole_primary_domain_info_level">DSROLE_PRIMARY_DOMAIN_INFO_LEVEL</a> values that specify the type of data to retrieve. This parameter also determines the format of the data supplied in <i>Buffer</i>.

### -param Buffer [out]

Pointer to the address of a buffer that receives the requested data. The format of this data depends on the value of the <i>InfoLevel</i> parameter.

The caller must free this memory when it is no longer required by calling <a href="/windows/desktop/api/dsrole/nf-dsrole-dsrolefreememory">DsRoleFreeMemory</a>.

## -returns

If the function is successful, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value can be one of the following values.

## -see-also

<a href="/windows/desktop/api/dsrole/ns-dsrole-dsrole_operation_state_info">DSROLE_OPERATION_STATE_INFO</a>



<a href="/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic">DSROLE_PRIMARY_DOMAIN_INFO_BASIC</a>



<a href="/windows/desktop/api/dsrole/ns-dsrole-dsrole_upgrade_status_info">DSROLE_UPGRADE_STATUS_INFO</a>



<a href="/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="/windows/desktop/api/dsrole/nf-dsrole-dsrolefreememory">DsRoleFreeMemory</a>