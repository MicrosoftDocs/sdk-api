---
UID: NE:taskschd._TASK_LOGON_TYPE
title: TASK_LOGON_TYPE (taskschd.h)
description: Defines what logon technique is required to run a task.
helpviewer_keywords: ["TASK_LOGON_GROUP","TASK_LOGON_INTERACTIVE_TOKEN","TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD","TASK_LOGON_NONE","TASK_LOGON_PASSWORD","TASK_LOGON_S4U","TASK_LOGON_SERVICE_ACCOUNT","TASK_LOGON_TYPE","TASK_LOGON_TYPE enumeration [Task Scheduler]","taskschd.task_logon_type","taskschd/TASK_LOGON_GROUP","taskschd/TASK_LOGON_INTERACTIVE_TOKEN","taskschd/TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD","taskschd/TASK_LOGON_NONE","taskschd/TASK_LOGON_PASSWORD","taskschd/TASK_LOGON_S4U","taskschd/TASK_LOGON_SERVICE_ACCOUNT","taskschd/TASK_LOGON_TYPE"]
old-location: taskschd\task_logon_type.htm
tech.root: taskschd
ms.assetid: 93952769-6076-4e71-9ea4-d7e7c3c908d8
ms.date: 12/05/2018
ms.keywords: TASK_LOGON_GROUP, TASK_LOGON_INTERACTIVE_TOKEN, TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD, TASK_LOGON_NONE, TASK_LOGON_PASSWORD, TASK_LOGON_S4U, TASK_LOGON_SERVICE_ACCOUNT, TASK_LOGON_TYPE, TASK_LOGON_TYPE enumeration [Task Scheduler], taskschd.task_logon_type, taskschd/TASK_LOGON_GROUP, taskschd/TASK_LOGON_INTERACTIVE_TOKEN, taskschd/TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD, taskschd/TASK_LOGON_NONE, taskschd/TASK_LOGON_PASSWORD, taskschd/TASK_LOGON_S4U, taskschd/TASK_LOGON_SERVICE_ACCOUNT, taskschd/TASK_LOGON_TYPE
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
targetos: Windows
req.typenames: TASK_LOGON_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASK_LOGON_TYPE
 - taskschd/_TASK_LOGON_TYPE
 - TASK_LOGON_TYPE
 - taskschd/TASK_LOGON_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - taskschd.h
api_name:
 - TASK_LOGON_TYPE
---

# TASK_LOGON_TYPE enumeration


## -description

Defines what logon technique is required to run a task.

## -enum-fields

### -field TASK_LOGON_NONE:0

The logon method is not specified. Used for non-NT credentials.

### -field TASK_LOGON_PASSWORD:1

Use a password for logging on the user. The password must be supplied at registration time.

### -field TASK_LOGON_S4U:2

The service will log the user on using Service For User (S4U), and the task will run in a non-interactive desktop.  When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.

### -field TASK_LOGON_INTERACTIVE_TOKEN:3

 User must already be logged on. The task will be run only in an existing interactive session.

### -field TASK_LOGON_GROUP:4

Group activation. The <b>groupId</b> field specifies the group.

### -field TASK_LOGON_SERVICE_ACCOUNT:5

Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.

### -field TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD:6

Not in use; currently identical to TASK_LOGON_PASSWORD.

<b>Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista and Windows Server 2008:  </b>First use the interactive token.  If the user is not logged on (no interactive token is available), then the password is used.  The password must be specified when a task is registered. This flag is not recommended for new tasks because it is less reliable than TASK_LOGON_PASSWORD.

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
