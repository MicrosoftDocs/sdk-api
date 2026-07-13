---
UID: NF:azroles.IAzTask.AddOperation
title: IAzTask::AddOperation (azroles.h)
description: Adds the IAzOperation object with the specified name to the task.
helpviewer_keywords: ["AddOperation","AddOperation method [Security]","AddOperation method [Security]","AzTask object","AddOperation method [Security]","IAzTask interface","AzTask object [Security]","AddOperation method","IAzTask interface [Security]","AddOperation method","IAzTask.AddOperation","IAzTask::AddOperation","azroles/IAzTask::AddOperation","security.iaztask_addoperation"]
old-location: security\iaztask_addoperation.htm
tech.root: security
ms.assetid: 73da7094-440c-4e68-8d43-9f4ba26dd14b
ms.date: 03/20/2023
ms.keywords: AddOperation, AddOperation method [Security], AddOperation method [Security],AzTask object, AddOperation method [Security],IAzTask interface, AzTask object [Security],AddOperation method, IAzTask interface [Security],AddOperation method, IAzTask.AddOperation, IAzTask::AddOperation, azroles/IAzTask::AddOperation, security.iaztask_addoperation
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
 - IAzTask::AddOperation
 - azroles/IAzTask::AddOperation
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
 - IAzTask.AddOperation
 - AzTask.AddOperation
---

# IAzTask::AddOperation

## -description

The **AddOperation** method adds the [IAzOperation](nn-azroles-iazoperation.md) object with the specified name to the task.

## -parameters

### -param bstrOp [in]

Name of the [IAzOperation](nn-azroles-iazoperation.md) object to add to the task.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

You must call the [Submit](nf-azroles-iaztask-submit.md) method to persist any changes made by this method.

## -see-also

[IAzOperation](nn-azroles-iazoperation.md)

[Submit](nf-azroles-iaztask-submit.md)
