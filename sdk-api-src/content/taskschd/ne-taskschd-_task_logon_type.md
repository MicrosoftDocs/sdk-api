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

# _TASK_LOGON_TYPE enumeration


## -description


Defines what logon technique is required to run a task.


## -enum-fields




### -field TASK_LOGON_NONE

The logon method is not specified. Used for non-NT credentials.


### -field TASK_LOGON_PASSWORD

Use a password for logging on the user. The password must be supplied at registration time.


### -field TASK_LOGON_S4U

The service will log the user on using Service For User (S4U), and the task will run in a non-interactive desktop.  When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.


### -field TASK_LOGON_INTERACTIVE_TOKEN

 User must already be logged on. The task will be run only in an existing interactive session.


### -field TASK_LOGON_GROUP

Group activation. The <b>groupId</b> field specifies the group.


### -field TASK_LOGON_SERVICE_ACCOUNT

Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.


### -field TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD

Not in use; currently identical to TASK_LOGON_PASSWORD.

<b>Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista and Windows Server 2008:  </b>First use the interactive token.  If the user is not logged on (no interactive token is available), then the password is used.  The password must be specified when a task is registered. This flag is not recommended for new tasks because it is less reliable than TASK_LOGON_PASSWORD.




## -see-also




<a href="https://msdn.microsoft.com/9779d32b-0142-41bb-88e2-df79a3b0c1b2">Task Scheduler Enumerated Types</a>
 

 

