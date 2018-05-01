---
UID: NS:dsrole._DSROLE_OPERATION_STATE_INFO
title: "_DSROLE_OPERATION_STATE_INFO"
author: windows-driver-content
description: Used with the DsRoleGetPrimaryDomainInformation function to contain the operational state data for a computer.
old-location: ad\dsrole_operation_state_info.htm
old-project: AD
ms.assetid: c6c8e510-190a-47ad-805c-b8d3fbee836d
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: "*PDSROLE_OPERATION_STATE_INFO, DSROLE_OPERATION_STATE_INFO, DSROLE_OPERATION_STATE_INFO structure [Active Directory], _DSROLE_OPERATION_STATE_INFO, ad.dsrole_operation_state_info, dsrole/DSROLE_OPERATION_STATE_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DSROLE_OPERATION_STATE_INFO, *PDSROLE_OPERATION_STATE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dsrole.h
api_name:
-	DSROLE_OPERATION_STATE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DSROLE_OPERATION_STATE_INFO structure


## -description


The <b>DSROLE_OPERATION_STATE_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a> function to contain the operational state data for a computer.


## -struct-fields




### -field OperationState

Contains one of the <a href="https://msdn.microsoft.com/de294893-e78a-4b51-9a48-0c71f91b6fde">DSROLE_OPERATION_STATE</a> values that indicates the computer operational state.


## -see-also




<a href="https://msdn.microsoft.com/de294893-e78a-4b51-9a48-0c71f91b6fde">DSROLE_OPERATION_STATE</a>



<a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

