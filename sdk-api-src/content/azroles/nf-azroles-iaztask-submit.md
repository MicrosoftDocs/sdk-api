---
UID: NF:azroles.IAzTask.Submit
title: IAzTask::Submit (azroles.h)
description: Persists changes made to the IAzTask object.
helpviewer_keywords: ["AzTask object [Security]","Submit method","IAzTask interface [Security]","Submit method","IAzTask.Submit","IAzTask::Submit","Submit","Submit method [Security]","Submit method [Security]","AzTask object","Submit method [Security]","IAzTask interface","azroles/IAzTask::Submit","security.iaztask_submit"]
old-location: security\iaztask_submit.htm
tech.root: security
ms.assetid: a6f01573-c1ee-421d-8591-e1c9fa6c3d68
ms.date: 03/20/2023
ms.keywords: AzTask object [Security],Submit method, IAzTask interface [Security],Submit method, IAzTask.Submit, IAzTask::Submit, Submit, Submit method [Security], Submit method [Security],AzTask object, Submit method [Security],IAzTask interface, azroles/IAzTask::Submit, security.iaztask_submit
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
 - IAzTask::Submit
 - azroles/IAzTask::Submit
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
 - IAzTask.Submit
 - AzTask.Submit
---

# IAzTask::Submit

## -description

The **Submit** method persists changes made to the [IAzTask](nn-azroles-iaztask.md) object.

## -parameters

### -param lFlags [in, optional]

Flags that modify the behavior of the **Submit** method. The default value is zero. If the **AZ_SUBMIT_FLAG_ABORT** flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Any additions or modifications to an [IAzTask](nn-azroles-iaztask.md) object are not persisted until the **Submit** method is called.

## -see-also

[IAzTask](nn-azroles-iaztask.md)
