---
UID: NF:azroles.IAzRole.Submit
title: IAzRole::Submit (azroles.h)
description: Persists changes made to the IAzRole object.
helpviewer_keywords: ["AzRole object [Security]","Submit method","IAzRole interface [Security]","Submit method","IAzRole.Submit","IAzRole::Submit","Submit","Submit method [Security]","Submit method [Security]","AzRole object","Submit method [Security]","IAzRole interface","azroles/IAzRole::Submit","security.iazrole_submit"]
old-location: security\iazrole_submit.htm
tech.root: security
ms.assetid: 97f2018a-92f0-4ebb-85f1-78c140003d8f
ms.date: 03/20/2023
ms.keywords: AzRole object [Security],Submit method, IAzRole interface [Security],Submit method, IAzRole.Submit, IAzRole::Submit, Submit, Submit method [Security], Submit method [Security],AzRole object, Submit method [Security],IAzRole interface, azroles/IAzRole::Submit, security.iazrole_submit
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
 - IAzRole::Submit
 - azroles/IAzRole::Submit
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
 - IAzRole.Submit
 - AzRole.Submit
---

# IAzRole::Submit

## -description

The **Submit** method persists changes made to the [IAzRole](nn-azroles-iazrole.md) object.

## -parameters

### -param lFlags [in, optional]

Flags that modify the behavior of the **Submit** method. The default value is zero. If the **AZ_SUBMIT_FLAG_ABORT** flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Any additions or modifications to an [IAzRole](nn-azroles-iazrole.md) object are not persisted until the **Submit** method is called.

## -see-also

[IAzRole](nn-azroles-iazrole.md)
