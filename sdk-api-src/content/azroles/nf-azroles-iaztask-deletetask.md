---
UID: NF:azroles.IAzTask.DeleteTask
title: IAzTask::DeleteTask (azroles.h)
description: Removes the IAzTask object with the specified name from the task.
helpviewer_keywords: ["AzTask object [Security]","DeleteTask method","DeleteTask","DeleteTask method [Security]","DeleteTask method [Security]","AzTask object","DeleteTask method [Security]","IAzTask interface","IAzTask interface [Security]","DeleteTask method","IAzTask.DeleteTask","IAzTask::DeleteTask","azroles/IAzTask::DeleteTask","security.iaztask_deletetask"]
old-location: security\iaztask_deletetask.htm
tech.root: security
ms.assetid: 1e1288ff-d67b-4180-bfd0-63b81df8f99b
ms.date: 12/05/2018
ms.keywords: AzTask object [Security],DeleteTask method, DeleteTask, DeleteTask method [Security], DeleteTask method [Security],AzTask object, DeleteTask method [Security],IAzTask interface, IAzTask interface [Security],DeleteTask method, IAzTask.DeleteTask, IAzTask::DeleteTask, azroles/IAzTask::DeleteTask, security.iaztask_deletetask
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
 - IAzTask::DeleteTask
 - azroles/IAzTask::DeleteTask
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
 - IAzTask.DeleteTask
 - AzTask.DeleteTask
---

# IAzTask::DeleteTask


## -description

The <b>DeleteTask</b> method removes the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name from the task.

## -parameters

### -param bstrTask [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object to remove from the task.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

If there are any <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> references to an <b>IAzTask</b> object that has been deleted from the cache, the <b>IAzTask</b> object can no longer be used. In C++, you must release references to deleted <b>IAzTask</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.