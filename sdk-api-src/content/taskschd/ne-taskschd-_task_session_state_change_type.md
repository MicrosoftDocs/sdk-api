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

# _TASK_SESSION_STATE_CHANGE_TYPE enumeration


## -description


Defines what kind of Terminal Server session state change you can use to trigger a task to start. These changes are used to specify the type of state change in the <a href="https://msdn.microsoft.com/0bf56d67-6c44-4978-93a9-7b525f2bf140">ISessionStateChangeTrigger</a> interface.


## -enum-fields




### -field TASK_CONSOLE_CONNECT

Terminal Server console connection state change. For example, when you connect to a user session on the local computer by switching users on the computer.


### -field TASK_CONSOLE_DISCONNECT

Terminal Server console disconnection state change. For example, when you disconnect to a user session on the local computer by switching users on the computer.


### -field TASK_REMOTE_CONNECT

Terminal Server remote connection state change. For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.


### -field TASK_REMOTE_DISCONNECT

Terminal Server remote disconnection state change. For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.


### -field TASK_SESSION_LOCK

Terminal Server session locked state change. For example, this state change causes the task to run when the computer is locked.


### -field TASK_SESSION_UNLOCK

Terminal Server session unlocked state change. For example, this state change causes the task to run when the computer is unlocked.


## -see-also




<a href="https://msdn.microsoft.com/0bf56d67-6c44-4978-93a9-7b525f2bf140">ISessionStateChangeTrigger</a>



<a href="https://msdn.microsoft.com/9779d32b-0142-41bb-88e2-df79a3b0c1b2">Task Scheduler Enumerated Types</a>
 

 

