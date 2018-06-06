---
UID: NE:taskschd._TASK_PROCESSTOKENSID
title: "_TASK_PROCESSTOKENSID"
author: windows-sdk-content
description: Defines the types of process security identifier (SID) that can be used by tasks.
old-location: taskschd\task_processtokensid_type.htm
old-project: TaskSchd
ms.assetid: 3a9243b9-f764-430b-8184-1fd97e74a5f1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: TASK_PROCESSTOKENSID_DEFAULT, TASK_PROCESSTOKENSID_NONE, TASK_PROCESSTOKENSID_TYPE, TASK_PROCESSTOKENSID_TYPE enumeration [Task Scheduler], TASK_PROCESSTOKENSID_UNRESTRICTED, _TASK_PROCESSTOKENSID, taskschd.task_processtokensid_type, taskschd/TASK_PROCESSTOKENSID_DEFAULT, taskschd/TASK_PROCESSTOKENSID_NONE, taskschd/TASK_PROCESSTOKENSID_TYPE, taskschd/TASK_PROCESSTOKENSID_UNRESTRICTED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: TASK_PROCESSTOKENSID_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - taskschd.h
api_name:
 - TASK_PROCESSTOKENSID_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

