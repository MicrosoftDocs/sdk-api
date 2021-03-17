---
UID: NF:azroles.IAzTask.DeleteOperation
title: IAzTask::DeleteOperation (azroles.h)
description: Removes the IAzOperation object with the specified name from the task.
helpviewer_keywords: ["AzTask object [Security]","DeleteOperation method","DeleteOperation","DeleteOperation method [Security]","DeleteOperation method [Security]","AzTask object","DeleteOperation method [Security]","IAzTask interface","IAzTask interface [Security]","DeleteOperation method","IAzTask.DeleteOperation","IAzTask::DeleteOperation","azroles/IAzTask::DeleteOperation","security.iaztask_deleteoperation"]
old-location: security\iaztask_deleteoperation.htm
tech.root: security
ms.assetid: 3f370d04-2115-4dcc-bf18-2d28a52bdead
ms.date: 12/05/2018
ms.keywords: AzTask object [Security],DeleteOperation method, DeleteOperation, DeleteOperation method [Security], DeleteOperation method [Security],AzTask object, DeleteOperation method [Security],IAzTask interface, IAzTask interface [Security],DeleteOperation method, IAzTask.DeleteOperation, IAzTask::DeleteOperation, azroles/IAzTask::DeleteOperation, security.iaztask_deleteoperation
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
 - IAzTask::DeleteOperation
 - azroles/IAzTask::DeleteOperation
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
 - IAzTask.DeleteOperation
 - AzTask.DeleteOperation
---

# IAzTask::DeleteOperation


## -description

The <b>DeleteOperation</b> method removes the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name from the task.

## -parameters

### -param bstrOp [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object to remove from the task.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

If there are any <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> references to an <b>IAzOperation</b> object that has been deleted from the cache, the <b>IAzOperation</b> object can no longer be used. In C++, you must release references to deleted <b>IAzOperation</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.