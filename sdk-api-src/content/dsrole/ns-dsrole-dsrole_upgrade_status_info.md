---
UID: NS:dsrole._DSROLE_UPGRADE_STATUS_INFO
title: DSROLE_UPGRADE_STATUS_INFO (dsrole.h)
description: Used with the DsRoleGetPrimaryDomainInformation function to contain domain upgrade status data.
helpviewer_keywords: ["*PDSROLE_UPGRADE_STATUS_INFO","0","DSROLE_UPGRADE_IN_PROGRESS","DSROLE_UPGRADE_STATUS_INFO","DSROLE_UPGRADE_STATUS_INFO structure [Active Directory]","PDSROLE_UPGRADE_STATUS_INFO","PDSROLE_UPGRADE_STATUS_INFO structure pointer [Active Directory]","_glines_dsrole_upgrade_status_info","ad.dsrole__upgrade__status__info","ad.dsrole_upgrade_status_info","dsrole/DSROLE_UPGRADE_STATUS_INFO","dsrole/PDSROLE_UPGRADE_STATUS_INFO"]
old-location: ad\dsrole_upgrade_status_info.htm
tech.root: ad
ms.assetid: c368d8d9-a91d-4013-880e-36a47d42a697
ms.date: 12/05/2018
ms.keywords: '*PDSROLE_UPGRADE_STATUS_INFO, 0, DSROLE_UPGRADE_IN_PROGRESS, DSROLE_UPGRADE_STATUS_INFO, DSROLE_UPGRADE_STATUS_INFO structure [Active Directory], PDSROLE_UPGRADE_STATUS_INFO, PDSROLE_UPGRADE_STATUS_INFO structure pointer [Active Directory], _glines_dsrole_upgrade_status_info, ad.dsrole__upgrade__status__info, ad.dsrole_upgrade_status_info, dsrole/DSROLE_UPGRADE_STATUS_INFO, dsrole/PDSROLE_UPGRADE_STATUS_INFO'
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSROLE_UPGRADE_STATUS_INFO
 - dsrole/_DSROLE_UPGRADE_STATUS_INFO
 - PDSROLE_UPGRADE_STATUS_INFO
 - dsrole/PDSROLE_UPGRADE_STATUS_INFO
 - DSROLE_UPGRADE_STATUS_INFO
 - dsrole/DSROLE_UPGRADE_STATUS_INFO
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
 - DSROLE_UPGRADE_STATUS_INFO
---

# DSROLE_UPGRADE_STATUS_INFO structure


## -description

The <b>DSROLE_UPGRADE_STATUS_INFO</b> structure is used with the <a href="/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a> function to contain domain upgrade status data.

## -struct-fields

### -field OperationState

Specifies the current state of the upgrade. This member can be one of the following values.



#### 0

An upgrade is not in progress.



#### DSROLE_UPGRADE_IN_PROGRESS

An upgrade is in progress.

### -field PreviousServerState

If an upgrade is in progress, this member contains one of the <a href="/windows/desktop/api/dsrole/ne-dsrole-dsrole_server_state">DSROLE_SERVER_STATE</a> values that indicate the previous role of the server.

## -see-also

<a href="/windows/desktop/AD/directory-service-structures">Directory Service Structures</a>



<a href="/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a>