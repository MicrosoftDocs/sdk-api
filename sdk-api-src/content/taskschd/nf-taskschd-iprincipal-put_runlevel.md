---
UID: NF:taskschd.IPrincipal.put_RunLevel
title: IPrincipal::put_RunLevel (taskschd.h)
description: Gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.helpviewer_keywords: ["IPrincipal interface [Task Scheduler]","RunLevel property","IPrincipal.RunLevel","IPrincipal.put_RunLevel","IPrincipal::RunLevel","IPrincipal::get_RunLevel","IPrincipal::put_RunLevel","RunLevel property [Task Scheduler]","RunLevel property [Task Scheduler]","IPrincipal interface","TASK_RUNLEVEL_HIGHEST","TASK_RUNLEVEL_LUA","put_RunLevel","taskschd.iprincipal_runlevel","taskschd/IPrincipal::RunLevel","taskschd/IPrincipal::get_RunLevel","taskschd/IPrincipal::put_RunLevel"]
old-location: taskschd\iprincipal_runlevel.htm
tech.root: taskschd
ms.assetid: 90f2dcfc-4704-4731-9b86-12a2a6f208f4
ms.date: 12/05/2018
ms.keywords: IPrincipal interface [Task Scheduler],RunLevel property, IPrincipal.RunLevel, IPrincipal.put_RunLevel, IPrincipal::RunLevel, IPrincipal::get_RunLevel, IPrincipal::put_RunLevel, RunLevel property [Task Scheduler], RunLevel property [Task Scheduler],IPrincipal interface, TASK_RUNLEVEL_HIGHEST, TASK_RUNLEVEL_LUA, put_RunLevel, taskschd.iprincipal_runlevel, taskschd/IPrincipal::RunLevel, taskschd/IPrincipal::get_RunLevel, taskschd/IPrincipal::put_RunLevel
f1_keywords:
- taskschd/IPrincipal.RunLevel
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- taskschd.dll
api_name:
- IPrincipal.RunLevel
- IPrincipal.get_RunLevel
- IPrincipal.put_RunLevel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPrincipal::put_RunLevel


## -description


Gets or sets the identifier that is used to specify  the privilege level that is required to run the tasks that are associated with the principal.

This property is read/write.


## -parameters


## -remarks



If a task is registered using the Builtin\Administrator account or the Local System or Local Service accounts, then the <b>RunLevel</b> property will be ignored.  The property value will also be ignored if User Account Control (UAC) is turned off.

If a task is registered using the Administrators group for the security context of the task, then you must also set the <b>RunLevel</b> property to <b>TASK_RUNLEVEL_HIGHEST</b> if you want to run the task. For more information, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/security-contexts-for-running-tasks">Security Contexts for  Tasks</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iprincipal">IPrincipal</a>
 

 

