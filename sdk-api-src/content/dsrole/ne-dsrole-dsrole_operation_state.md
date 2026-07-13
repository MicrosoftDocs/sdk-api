---
UID: NE:dsrole._DSROLE_OPERATION_STATE
title: DSROLE_OPERATION_STATE (dsrole.h)
description: Used with the DSROLE_OPERATION_STATE_INFO structure to indicate the operational state of a computer.
helpviewer_keywords: ["DSROLE_OPERATION_STATE","DSROLE_OPERATION_STATE enumeration [Active Directory]","DsRoleOperationActive","DsRoleOperationIdle","DsRoleOperationNeedReboot","ad.dsrole_operation_state","dsrole/DSROLE_OPERATION_STATE","dsrole/DsRoleOperationActive","dsrole/DsRoleOperationIdle","dsrole/DsRoleOperationNeedReboot"]
old-location: ad\dsrole_operation_state.htm
tech.root: ad
ms.assetid: de294893-e78a-4b51-9a48-0c71f91b6fde
ms.date: 12/05/2018
ms.keywords: DSROLE_OPERATION_STATE, DSROLE_OPERATION_STATE enumeration [Active Directory], DsRoleOperationActive, DsRoleOperationIdle, DsRoleOperationNeedReboot, ad.dsrole_operation_state, dsrole/DSROLE_OPERATION_STATE, dsrole/DsRoleOperationActive, dsrole/DsRoleOperationIdle, dsrole/DsRoleOperationNeedReboot
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
req.typenames: DSROLE_OPERATION_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSROLE_OPERATION_STATE
 - dsrole/_DSROLE_OPERATION_STATE
 - DSROLE_OPERATION_STATE
 - dsrole/DSROLE_OPERATION_STATE
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
 - DSROLE_OPERATION_STATE
---

# DSROLE_OPERATION_STATE enumeration


## -description

The <b>DSROLE_OPERATION_STATE</b> enumeration is used with the <a href="/windows/desktop/api/dsrole/ns-dsrole-dsrole_operation_state_info">DSROLE_OPERATION_STATE_INFO</a> structure to indicate the operational state of a computer.

## -enum-fields

### -field DsRoleOperationIdle:0

The computer is idle.

### -field DsRoleOperationActive

The computer is active.

### -field DsRoleOperationNeedReboot

The computer requires a restart.

## -see-also

<a href="/windows/desktop/api/dsrole/ns-dsrole-dsrole_operation_state_info">DSROLE_OPERATION_STATE_INFO</a>



<a href="/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>
