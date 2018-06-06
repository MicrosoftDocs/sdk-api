---
UID: NE:dsrole._DSROLE_OPERATION_STATE
title: "_DSROLE_OPERATION_STATE"
author: windows-sdk-content
description: Used with the DSROLE_OPERATION_STATE_INFO structure to indicate the operational state of a computer.
old-location: ad\dsrole_operation_state.htm
old-project: AD
ms.assetid: de294893-e78a-4b51-9a48-0c71f91b6fde
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DSROLE_OPERATION_STATE, DSROLE_OPERATION_STATE enumeration [Active Directory], DsRoleOperationActive, DsRoleOperationIdle, DsRoleOperationNeedReboot, _DSROLE_OPERATION_STATE, ad.dsrole_operation_state, dsrole/DSROLE_OPERATION_STATE, dsrole/DsRoleOperationActive, dsrole/DsRoleOperationIdle, dsrole/DsRoleOperationNeedReboot
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: DSROLE_OPERATION_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsrole.h
api_name:
 - DSROLE_OPERATION_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DSROLE_OPERATION_STATE enumeration


## -description


The <b>DSROLE_OPERATION_STATE</b> enumeration is used with the <a href="https://msdn.microsoft.com/c6c8e510-190a-47ad-805c-b8d3fbee836d">DSROLE_OPERATION_STATE_INFO</a> structure to indicate the operational state of a computer.


## -enum-fields




### -field DsRoleOperationIdle

The computer is idle.


### -field DsRoleOperationActive

The computer is active.


### -field DsRoleOperationNeedReboot

The computer requires a restart.


## -see-also




<a href="https://msdn.microsoft.com/c6c8e510-190a-47ad-805c-b8d3fbee836d">DSROLE_OPERATION_STATE_INFO</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

