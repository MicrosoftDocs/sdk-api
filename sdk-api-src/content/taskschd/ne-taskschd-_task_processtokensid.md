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

# _TASK_PROCESSTOKENSID enumeration


## -description


Defines the types of process security identifier (SID) that can be used by tasks. These changes are used to specify the type of process SID in the <a href="https://msdn.microsoft.com/480f8038-0f67-4a69-b6f6-d7ba881d9d57">IPrincipal2</a> interface.


## -enum-fields




### -field TASK_PROCESSTOKENSID_NONE

No changes will be made to the process token groups list. 


### -field TASK_PROCESSTOKENSID_UNRESTRICTED

A task SID that is derived from the task name will be added to the process token groups list, and  the token default discretionary access control list (DACL) will be modified to allow only the task SID and local system full control and the account SID read control.


### -field TASK_PROCESSTOKENSID_DEFAULT

A Task Scheduler will apply default settings to the task process.


## -see-also




<a href="https://msdn.microsoft.com/480f8038-0f67-4a69-b6f6-d7ba881d9d57">IPrincipal2</a>



<a href="https://msdn.microsoft.com/9779d32b-0142-41bb-88e2-df79a3b0c1b2">Task Scheduler Enumerated Types</a>
 

 

