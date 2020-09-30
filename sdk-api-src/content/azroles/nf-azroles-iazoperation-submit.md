---
UID: NF:azroles.IAzOperation.Submit
title: IAzOperation::Submit (azroles.h)
description: Persists changes made to the IAzOperation object.
helpviewer_keywords: ["AzOperation object [Security]","Submit method","IAzOperation interface [Security]","Submit method","IAzOperation.Submit","IAzOperation::Submit","Submit","Submit method [Security]","Submit method [Security]","AzOperation object","Submit method [Security]","IAzOperation interface","azroles/IAzOperation::Submit","security.iazoperation_submit"]
old-location: security\iazoperation_submit.htm
tech.root: security
ms.assetid: f6265bfa-c856-47db-a688-f5de25ef7157
ms.date: 12/05/2018
ms.keywords: AzOperation object [Security],Submit method, IAzOperation interface [Security],Submit method, IAzOperation.Submit, IAzOperation::Submit, Submit, Submit method [Security], Submit method [Security],AzOperation object, Submit method [Security],IAzOperation interface, azroles/IAzOperation::Submit, security.iazoperation_submit
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
 - IAzOperation::Submit
 - azroles/IAzOperation::Submit
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
 - IAzOperation.Submit
 - AzOperation.Submit
---

# IAzOperation::Submit


## -description

The <b>Submit</b> method persists changes made to the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object.

## -parameters

### -param lFlags [in, optional]

Flags that modify the behavior of the <b>Submit</b> method. The default value is zero. If the AZ_SUBMIT_FLAG_ABORT flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

Any additions or modifications to an <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object are not persisted until the <b>Submit</b> method is called.