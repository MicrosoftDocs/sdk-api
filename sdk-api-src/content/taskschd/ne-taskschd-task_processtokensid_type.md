---
UID: NE:taskschd._TASK_PROCESSTOKENSID
title: TASK_PROCESSTOKENSID_TYPE (taskschd.h)
description: Defines the types of process security identifier (SID) that can be used by tasks.
helpviewer_keywords: ["TASK_PROCESSTOKENSID_DEFAULT","TASK_PROCESSTOKENSID_NONE","TASK_PROCESSTOKENSID_TYPE","TASK_PROCESSTOKENSID_TYPE enumeration [Task Scheduler]","TASK_PROCESSTOKENSID_UNRESTRICTED","taskschd.task_processtokensid_type","taskschd/TASK_PROCESSTOKENSID_DEFAULT","taskschd/TASK_PROCESSTOKENSID_NONE","taskschd/TASK_PROCESSTOKENSID_TYPE","taskschd/TASK_PROCESSTOKENSID_UNRESTRICTED"]
old-location: taskschd\task_processtokensid_type.htm
tech.root: taskschd
ms.assetid: 3a9243b9-f764-430b-8184-1fd97e74a5f1
ms.date: 12/05/2018
ms.keywords: TASK_PROCESSTOKENSID_DEFAULT, TASK_PROCESSTOKENSID_NONE, TASK_PROCESSTOKENSID_TYPE, TASK_PROCESSTOKENSID_TYPE enumeration [Task Scheduler], TASK_PROCESSTOKENSID_UNRESTRICTED, taskschd.task_processtokensid_type, taskschd/TASK_PROCESSTOKENSID_DEFAULT, taskschd/TASK_PROCESSTOKENSID_NONE, taskschd/TASK_PROCESSTOKENSID_TYPE, taskschd/TASK_PROCESSTOKENSID_UNRESTRICTED
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TASK_PROCESSTOKENSID_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASK_PROCESSTOKENSID
 - taskschd/_TASK_PROCESSTOKENSID
 - TASK_PROCESSTOKENSID_TYPE
 - taskschd/TASK_PROCESSTOKENSID_TYPE
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
 - TASK_PROCESSTOKENSID_TYPE
---

# TASK_PROCESSTOKENSID_TYPE enumeration


## -description

Defines the types of process security identifier (SID) that can be used by tasks. These changes are used to specify the type of process SID in the <a href="/windows/desktop/api/taskschd/nn-taskschd-iprincipal2">IPrincipal2</a> interface.

## -enum-fields

### -field TASK_PROCESSTOKENSID_NONE:0

No changes will be made to the process token groups list.

### -field TASK_PROCESSTOKENSID_UNRESTRICTED:1

A task SID that is derived from the task name will be added to the process token groups list, and  the token default discretionary access control list (DACL) will be modified to allow only the task SID and local system full control and the account SID read control.

### -field TASK_PROCESSTOKENSID_DEFAULT:2

A Task Scheduler will apply default settings to the task process.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iprincipal2">IPrincipal2</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
