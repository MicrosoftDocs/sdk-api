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

# tagREPAIR_STATUS enumeration


## -description


The <b>REPAIR_STATUS</b> enumeration describes the result of a helper class attempting a repair option.


## -enum-fields




### -field RS_NOT_IMPLEMENTED

The helper class does not have a repair option implemented.


### -field RS_REPAIRED

The helper class has repaired a problem.


### -field RS_UNREPAIRED

The helper class has attempted to repair a problem but validation indicates the repair operation has not succeeded.


### -field RS_DEFERRED

The helper class is unable to perform the repair at this time.


### -field RS_USER_ACTION

The helper class needs the user to perform an action before the repair can continue.

