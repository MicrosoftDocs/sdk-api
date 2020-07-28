---
UID: NE:taskschd._TASK_SESSION_STATE_CHANGE_TYPE
title: TASK_SESSION_STATE_CHANGE_TYPE (taskschd.h)
description: Defines what kind of Terminal Server session state change you can use to trigger a task to start.
helpviewer_keywords: ["TASK_CONSOLE_CONNECT","TASK_CONSOLE_DISCONNECT","TASK_REMOTE_CONNECT","TASK_REMOTE_DISCONNECT","TASK_SESSION_LOCK","TASK_SESSION_STATE_CHANGE_TYPE","TASK_SESSION_STATE_CHANGE_TYPE enumeration [Task Scheduler]","TASK_SESSION_UNLOCK","taskschd.task_session_state_change_type","taskschd/TASK_CONSOLE_CONNECT","taskschd/TASK_CONSOLE_DISCONNECT","taskschd/TASK_REMOTE_CONNECT","taskschd/TASK_REMOTE_DISCONNECT","taskschd/TASK_SESSION_LOCK","taskschd/TASK_SESSION_STATE_CHANGE_TYPE","taskschd/TASK_SESSION_UNLOCK"]
old-location: taskschd\task_session_state_change_type.htm
tech.root: taskschd
ms.assetid: 275108c1-bc08-4856-8b4f-28f14bd519f7
ms.date: 12/05/2018
ms.keywords: TASK_CONSOLE_CONNECT, TASK_CONSOLE_DISCONNECT, TASK_REMOTE_CONNECT, TASK_REMOTE_DISCONNECT, TASK_SESSION_LOCK, TASK_SESSION_STATE_CHANGE_TYPE, TASK_SESSION_STATE_CHANGE_TYPE enumeration [Task Scheduler], TASK_SESSION_UNLOCK, taskschd.task_session_state_change_type, taskschd/TASK_CONSOLE_CONNECT, taskschd/TASK_CONSOLE_DISCONNECT, taskschd/TASK_REMOTE_CONNECT, taskschd/TASK_REMOTE_DISCONNECT, taskschd/TASK_SESSION_LOCK, taskschd/TASK_SESSION_STATE_CHANGE_TYPE, taskschd/TASK_SESSION_UNLOCK
f1_keywords:
- taskschd/TASK_SESSION_STATE_CHANGE_TYPE
dev_langs:
- c++
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- taskschd.h
api_name:
- TASK_SESSION_STATE_CHANGE_TYPE
targetos: Windows
req.typenames: TASK_SESSION_STATE_CHANGE_TYPE
req.redist: 
ms.custom: 19H1
---

# TASK_SESSION_STATE_CHANGE_TYPE enumeration


## -description


Defines what kind of Terminal Server session state change you can use to trigger a task to start. These changes are used to specify the type of state change in the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger">ISessionStateChangeTrigger</a> interface.


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




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger">ISessionStateChangeTrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
 

 

