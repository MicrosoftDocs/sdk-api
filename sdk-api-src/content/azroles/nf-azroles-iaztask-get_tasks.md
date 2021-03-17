---
UID: NF:azroles.IAzTask.get_Tasks
title: IAzTask::get_Tasks (azroles.h)
description: Retrieves the tasks associated with the task.
helpviewer_keywords: ["AzTask object [Security]","Tasks property","IAzTask interface [Security]","Tasks property","IAzTask.Tasks","IAzTask.get_Tasks","IAzTask::Tasks","IAzTask::get_Tasks","Tasks property [Security]","Tasks property [Security]","AzTask object","Tasks property [Security]","IAzTask interface","azroles/IAzTask::Tasks","azroles/IAzTask::get_Tasks","get_Tasks","security.iaztask_tasks"]
old-location: security\iaztask_tasks.htm
tech.root: security
ms.assetid: a4baa899-78eb-4a3b-bcc1-0b8c2831b10f
ms.date: 12/05/2018
ms.keywords: AzTask object [Security],Tasks property, IAzTask interface [Security],Tasks property, IAzTask.Tasks, IAzTask.get_Tasks, IAzTask::Tasks, IAzTask::get_Tasks, Tasks property [Security], Tasks property [Security],AzTask object, Tasks property [Security],IAzTask interface, azroles/IAzTask::Tasks, azroles/IAzTask::get_Tasks, get_Tasks, security.iaztask_tasks
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzTask::get_Tasks
 - azroles/IAzTask::get_Tasks
dev_langs:
 - c++
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
---

# IAzTask::get_Tasks


## -description

The <b>Tasks</b> property retrieves the tasks associated with the task.

This property is read-only.

## -parameters

## -remarks

This property shows the nesting of <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> objects within another <b>IAzTask</b> object.

In  JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.