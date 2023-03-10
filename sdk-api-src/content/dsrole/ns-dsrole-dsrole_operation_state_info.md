---
UID: NS:dsrole._DSROLE_OPERATION_STATE_INFO
title: DSROLE_OPERATION_STATE_INFO (dsrole.h)
description: Used with the DsRoleGetPrimaryDomainInformation function to contain the operational state data for a computer.
helpviewer_keywords: ["*PDSROLE_OPERATION_STATE_INFO","DSROLE_OPERATION_STATE_INFO","DSROLE_OPERATION_STATE_INFO structure [Active Directory]","ad.dsrole_operation_state_info","dsrole/DSROLE_OPERATION_STATE_INFO"]
old-location: ad\dsrole_operation_state_info.htm
tech.root: ad
ms.assetid: c6c8e510-190a-47ad-805c-b8d3fbee836d
ms.date: 12/05/2018
ms.keywords: '*PDSROLE_OPERATION_STATE_INFO, DSROLE_OPERATION_STATE_INFO, DSROLE_OPERATION_STATE_INFO structure [Active Directory], ad.dsrole_operation_state_info, dsrole/DSROLE_OPERATION_STATE_INFO'
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
req.typenames: DSROLE_OPERATION_STATE_INFO, *PDSROLE_OPERATION_STATE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSROLE_OPERATION_STATE_INFO
 - dsrole/_DSROLE_OPERATION_STATE_INFO
 - PDSROLE_OPERATION_STATE_INFO
 - dsrole/PDSROLE_OPERATION_STATE_INFO
 - DSROLE_OPERATION_STATE_INFO
 - dsrole/DSROLE_OPERATION_STATE_INFO
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
 - DSROLE_OPERATION_STATE_INFO
---

# DSROLE_OPERATION_STATE_INFO structure


## -description

The <b>DSROLE_OPERATION_STATE_INFO</b> structure is used with the <a href="/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a> function to contain the operational state data for a computer.

## -struct-fields

### -field OperationState

Contains one of the <a href="/windows/desktop/api/dsrole/ne-dsrole-dsrole_operation_state">DSROLE_OPERATION_STATE</a> values that indicates the computer operational state.

## -see-also

<a href="/windows/desktop/api/dsrole/ne-dsrole-dsrole_operation_state">DSROLE_OPERATION_STATE</a>



<a href="/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a>



<a href="/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>