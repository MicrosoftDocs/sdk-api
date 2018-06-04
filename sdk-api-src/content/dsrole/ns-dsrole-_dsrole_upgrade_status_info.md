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
 

 

