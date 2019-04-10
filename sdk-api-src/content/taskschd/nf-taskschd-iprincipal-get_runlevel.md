---
UID: NF:taskschd.IPrincipal.get_RunLevel
title: IPrincipal::get_RunLevel (taskschd.h)
author: windows-sdk-content
description: Gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.
old-location: taskschd\iprincipal_runlevel.htm
tech.root: taskschd
ms.assetid: 90f2dcfc-4704-4731-9b86-12a2a6f208f4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPrincipal interface [Task Scheduler],RunLevel property, IPrincipal.RunLevel, IPrincipal.get_RunLevel, IPrincipal::RunLevel, IPrincipal::get_RunLevel, IPrincipal::put_RunLevel, RunLevel property [Task Scheduler], RunLevel property [Task Scheduler],IPrincipal interface, TASK_RUNLEVEL_HIGHEST, TASK_RUNLEVEL_LUA, get_RunLevel, taskschd.iprincipal_runlevel, taskschd/IPrincipal::RunLevel, taskschd/IPrincipal::get_RunLevel, taskschd/IPrincipal::put_RunLevel
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrincipal::get_RunLevel


## -description


Gets or sets the identifier that is used to specify  the privilege level that is required to run the tasks that are associated with the principal.

This property is read/write.


## -parameters


## -remarks



If a task is registered using the Builtin\Administrator account or the Local System or Local Service accounts, then the <b>RunLevel</b> property will be ignored.  The property value will also be ignored if User Account Control (UAC) is turned off.

If a task is registered using the Administrators group for the security context of the task, then you must also set the <b>RunLevel</b> property to <b>TASK_RUNLEVEL_HIGHEST</b> if you want to run the task. For more information, see <a href="https://msdn.microsoft.com/be86eb9f-f6ec-4dce-afe8-e3314a74062a">Security Contexts for  Tasks</a>.




## -see-also




<a href="https://msdn.microsoft.com/7aa22af2-7f0a-41c1-89c6-d813780e89bf">IPrincipal</a>
 

 

