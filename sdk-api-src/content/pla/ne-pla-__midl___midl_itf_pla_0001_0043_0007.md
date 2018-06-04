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

# __MIDL___MIDL_itf_pla_0001_0043_0007 enumeration


## -description


Defines the action to take when committing changes to the data collector set.


## -enum-fields




### -field plaCreateNew

Save the set. The set must not already exist. 

The set is not saved if it is a trace session.


### -field plaModify

Update a previously saved set.


### -field plaCreateOrModify

Save the set. If the set already exists, update the set.

The set is not saved if it is a trace session.


### -field plaUpdateRunningInstance

Apply the updated property values to the currently running data set.


### -field plaFlushTrace

Flush the buffers for an Event Tracing for Windows trace session. This action applies only to sets that contain trace data collectors.


### -field plaValidateOnly

Perform validation only on the set.


## -remarks



All commit modes validate the set.




## -see-also




<a href="https://msdn.microsoft.com/7e432e1f-4b86-45dc-93d5-df603068273d">IDataCollectorSet::Commit</a>
 

 

