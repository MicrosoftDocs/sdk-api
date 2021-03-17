---
UID: NF:azroles.IAzTask.AddTask
title: IAzTask::AddTask (azroles.h)
description: Adds the IAzTask object with the specified name to the task.
helpviewer_keywords: ["AddTask","AddTask method [Security]","AddTask method [Security]","AzTask object","AddTask method [Security]","IAzTask interface","AzTask object [Security]","AddTask method","IAzTask interface [Security]","AddTask method","IAzTask.AddTask","IAzTask::AddTask","azroles/IAzTask::AddTask","security.iaztask_addtask"]
old-location: security\iaztask_addtask.htm
tech.root: security
ms.assetid: 6b3057d1-26aa-443c-857f-0057ef9d2072
ms.date: 12/05/2018
ms.keywords: AddTask, AddTask method [Security], AddTask method [Security],AzTask object, AddTask method [Security],IAzTask interface, AzTask object [Security],AddTask method, IAzTask interface [Security],AddTask method, IAzTask.AddTask, IAzTask::AddTask, azroles/IAzTask::AddTask, security.iaztask_addtask
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
 - IAzTask::AddTask
 - azroles/IAzTask::AddTask
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
 - IAzTask.AddTask
 - AzTask.AddTask
---

# IAzTask::AddTask


## -description

The <b>AddTask</b> method adds the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name to the task.

## -parameters

### -param bstrTask [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object to add to the task.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

This method allows the nesting of <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> objects within another <b>IAzTask</b> object.

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-submit">Submit</a> method to persist any changes made by this method.