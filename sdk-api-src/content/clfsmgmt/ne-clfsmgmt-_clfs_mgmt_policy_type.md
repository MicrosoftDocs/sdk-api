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

# _CLFS_MGMT_POLICY_TYPE enumeration


## -description


The <b>CLFS_MGMT_POLICY_TYPE</b> enumeration lists the valid policy types.


## -enum-fields




### -field ClfsMgmtPolicyMaximumSize

Specifies the maximum size of the log.


### -field ClfsMgmtPolicyMinimumSize

Specifies the minimum size of the log.


### -field ClfsMgmtPolicyNewContainerSize

Specifies the size of a new container.


### -field ClfsMgmtPolicyGrowthRate

Controls the rate of growth of the log. 


### -field ClfsMgmtPolicyLogTail

Controls the amount of space that   <a href="https://msdn.microsoft.com/dfa64e5e-55ef-4102-90d5-104b1a624267">LOG_TAIL_ADVANCE_CALLBACK</a> requests.


### -field ClfsMgmtPolicyAutoShrink

Controls the percentage of containers that are removed if the log is set to autogrow.


### -field ClfsMgmtPolicyAutoGrow

Indicates if the log should automatically shrink or grow.


### -field ClfsMgmtPolicyNewContainerPrefix

Controls the prefix given to a new container.


### -field ClfsMgmtPolicyNewContainerSuffix

Controls the suffix given to a new container.


### -field ClfsMgmtPolicyNewContainerExtension

Controls the extension given to a new container.


### -field ClfsMgmtPolicyInvalid




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541842">CLFS_MGMT_POLICY</a>
 

 

