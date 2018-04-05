---
UID: NS:dsrole._DSROLE_UPGRADE_STATUS_INFO
title: "_DSROLE_UPGRADE_STATUS_INFO"
author: windows-driver-content
description: Used with the DsRoleGetPrimaryDomainInformation function to contain domain upgrade status data.
old-location: ad\dsrole_upgrade_status_info.htm
old-project: AD
ms.assetid: c368d8d9-a91d-4013-880e-36a47d42a697
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PDSROLE_UPGRADE_STATUS_INFO, 0, DSROLE_UPGRADE_IN_PROGRESS, DSROLE_UPGRADE_STATUS_INFO, DSROLE_UPGRADE_STATUS_INFO structure [Active Directory], PDSROLE_UPGRADE_STATUS_INFO, PDSROLE_UPGRADE_STATUS_INFO structure pointer [Active Directory], _DSROLE_UPGRADE_STATUS_INFO, _glines_dsrole_upgrade_status_info, ad.dsrole__upgrade__status__info, ad.dsrole_upgrade_status_info, dsrole/DSROLE_UPGRADE_STATUS_INFO, dsrole/PDSROLE_UPGRADE_STATUS_INFO"
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dsrole.h
api_name:
-	DSROLE_UPGRADE_STATUS_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DSROLE_UPGRADE_STATUS_INFO structure


## -description


The <b>DSROLE_UPGRADE_STATUS_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a> function to contain domain upgrade status data.


## -struct-fields




### -field OperationState

Specifies the current state of the upgrade. This member can be one of the following values.



#### 0

An upgrade is not in progress.



#### DSROLE_UPGRADE_IN_PROGRESS

An upgrade is in progress.


### -field PreviousServerState

If an upgrade is in progress, this member contains one of the <a href="https://msdn.microsoft.com/cd15aa25-7a73-475f-b163-30e5dc1f52bd">DSROLE_SERVER_STATE</a> values that indicate the previous role of the server.


## -see-also




<a href="https://msdn.microsoft.com/4df5f356-a39b-40a4-9e62-994ad27df3a9">Directory Service Structures</a>



<a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a>
 

 

