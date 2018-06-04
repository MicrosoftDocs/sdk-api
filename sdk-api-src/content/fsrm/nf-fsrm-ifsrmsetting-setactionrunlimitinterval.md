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

# IFsrmSetting::SetActionRunLimitInterval


## -description


Sets the time that an action that uses the global run limit interval must wait before the action is run again.


## -parameters




### -param actionType [in]

The action type to limit. For possible values, see the <a href="https://msdn.microsoft.com/3e34395e-b8e6-4288-a040-dff6cf7f5fe6">FsrmActionType</a> enumeration.


### -param delayTimeMinutes [in]

The run limit interval, in minutes, to use for the action. The default is 60 minutes.


## -returns



The method returns the following return values.




## -remarks



Applies to actions that have the <a href="https://msdn.microsoft.com/3d5be77f-282f-479d-aa34-a8cb1c771951">IFsrmAction::RunLimitInterval</a> property set to –1.

This property specifies the interval that should occur before the action is run again if the global run limit interval is used. For example, if the interval has expired since the action last ran, the server will run the action again in response to an event; otherwise, the server cannot run the action again.




## -see-also




<a href="https://msdn.microsoft.com/0c27393a-9a84-4147-a7e0-582c0bf2d918">FsrmSetting</a>



<a href="https://msdn.microsoft.com/432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b">IFsrmSetting</a>
 

 

