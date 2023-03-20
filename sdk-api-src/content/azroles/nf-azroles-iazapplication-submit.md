---
UID: NF:azroles.IAzApplication.Submit
title: IAzApplication::Submit (azroles.h)
description: Persists changes made to the IAzApplication object.
helpviewer_keywords: ["AzApplication object [Security]","Submit method","IAzApplication interface [Security]","Submit method","IAzApplication.Submit","IAzApplication::Submit","Submit","Submit method [Security]","Submit method [Security]","AzApplication object","Submit method [Security]","IAzApplication interface","azroles/IAzApplication::Submit","security.iazapplication_submit"]
old-location: security\iazapplication_submit.htm
tech.root: security
ms.assetid: d00d55a1-884f-46c2-b80b-f90ce8f5c648
ms.date: 03/20/2023
ms.keywords: AzApplication object [Security],Submit method, IAzApplication interface [Security],Submit method, IAzApplication.Submit, IAzApplication::Submit, Submit, Submit method [Security], Submit method [Security],AzApplication object, Submit method [Security],IAzApplication interface, azroles/IAzApplication::Submit, security.iazapplication_submit
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
 - IAzApplication::Submit
 - azroles/IAzApplication::Submit
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
 - IAzApplication.Submit
 - AzApplication.Submit
---

# IAzApplication::Submit

## -description

The **Submit** method persists changes made to the [IAzApplication](nn-azroles-iazapplication.md) object.

## -parameters

### -param lFlags [in]

Flags that modify the behavior of the **Submit** method. The default value is zero. If the **AZ_SUBMIT_FLAG_ABORT** flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Any additions or modifications to an [IAzApplication](nn-azroles-iazapplication.md) object are not persisted until the **Submit** method is called.

The **Submit** method does not extend to child objects; child objects  must be individually persisted to the policy store. A created [IAzApplication](nn-azroles-iazapplication.md) object must be submitted before it can be referenced or become a parent object. The destructor for an object silently discards unsubmitted changes.

## -see-also

[IAzApplication](nn-azroles-iazapplication.md)
