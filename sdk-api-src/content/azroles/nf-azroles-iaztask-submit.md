---
UID: NF:azroles.IAzTask.Submit
title: IAzTask::Submit (azroles.h)
description: Persists changes made to the IAzTask object.helpviewer_keywords: ["AzTask object [Security]","Submit method","IAzTask interface [Security]","Submit method","IAzTask.Submit","IAzTask::Submit","Submit","Submit method [Security]","Submit method [Security]","AzTask object","Submit method [Security]","IAzTask interface","azroles/IAzTask::Submit","security.iaztask_submit"]
old-location: security\iaztask_submit.htm
tech.root: SecAuthZ
ms.assetid: a6f01573-c1ee-421d-8591-e1c9fa6c3d68
ms.date: 12/05/2018
ms.keywords: AzTask object [Security],Submit method, IAzTask interface [Security],Submit method, IAzTask.Submit, IAzTask::Submit, Submit, Submit method [Security], Submit method [Security],AzTask object, Submit method [Security],IAzTask interface, azroles/IAzTask::Submit, security.iaztask_submit
f1_keywords:
- azroles/IAzTask.Submit
dev_langs:
- c++
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
- IAzTask.Submit
- AzTask.Submit
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzTask::Submit


## -description


The <b>Submit</b> method persists changes made to the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object.


## -parameters




### -param lFlags [in, optional]

Flags that modify the behavior of the <b>Submit</b> method. The default value is zero. If the AZ_SUBMIT_FLAG_ABORT flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Any additions or modifications to an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object are not persisted until the <b>Submit</b> method is called.



