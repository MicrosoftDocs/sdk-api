---
UID: NF:azroles.IAzTask.get_Tasks
title: IAzTask::get_Tasks
author: windows-sdk-content
description: Retrieves the tasks associated with the task.
old-location: security\iaztask_tasks.htm
tech.root: SecAuthZ
ms.assetid: a4baa899-78eb-4a3b-bcc1-0b8c2831b10f
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AzTask object [Security],Tasks property, IAzTask interface [Security],Tasks property, IAzTask.Tasks, IAzTask.get_Tasks, IAzTask::Tasks, IAzTask::get_Tasks, Tasks property [Security], Tasks property [Security],AzTask object, Tasks property [Security],IAzTask interface, azroles/IAzTask::Tasks, azroles/IAzTask::get_Tasks, get_Tasks, security.iaztask_tasks
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzTask.Tasks
 - IAzTask.get_Tasks
 - AzTask.Tasks
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzTask::get_Tasks


## -description


The <b>Tasks</b> property retrieves the tasks associated with the task.

This property is read-only.


## -parameters


## -remarks



This property shows the nesting of <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> objects within another <b>IAzTask</b> object.

In  JScript, the returned <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> must be converted to the JScript <a href="https://msdn.microsoft.com/library/k4h76zbx(v=VS.85).aspx">Array</a> object. 



