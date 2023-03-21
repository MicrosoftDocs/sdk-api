---
UID: NF:azroles.IAzApplicationGroup.Submit
title: IAzApplicationGroup::Submit (azroles.h)
description: Persists changes made to the IAzApplicationGroup object.
helpviewer_keywords: ["AzApplicationGroup object [Security]","Submit method","IAzApplicationGroup interface [Security]","Submit method","IAzApplicationGroup.Submit","IAzApplicationGroup::Submit","Submit","Submit method [Security]","Submit method [Security]","AzApplicationGroup object","Submit method [Security]","IAzApplicationGroup interface","azroles/IAzApplicationGroup::Submit","security.iazapplicationgroup_submit"]
old-location: security\iazapplicationgroup_submit.htm
tech.root: security
ms.assetid: 51a855dd-4a90-4f7a-b32f-f91e3941655b
ms.date: 03/20/2023
ms.keywords: AzApplicationGroup object [Security],Submit method, IAzApplicationGroup interface [Security],Submit method, IAzApplicationGroup.Submit, IAzApplicationGroup::Submit, Submit, Submit method [Security], Submit method [Security],AzApplicationGroup object, Submit method [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::Submit, security.iazapplicationgroup_submit
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
 - IAzApplicationGroup::Submit
 - azroles/IAzApplicationGroup::Submit
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
 - IAzApplicationGroup.Submit
 - AzApplicationGroup.Submit
---

# IAzApplicationGroup::Submit

## -description

The **Submit** method persists changes made to the [IAzApplicationGroup](nn-azroles-iazapplicationgroup.md) object.

## -parameters

### -param lFlags [in, optional]

Flags that modify the behavior of the **Submit** method. The default value is zero. If the **AZ_SUBMIT_FLAG_ABORT** flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Any additions or modifications to an [IAzApplicationGroup](nn-azroles-iazapplicationgroup.md) object are not persisted until the **Submit** method is called.

A created [IAzApplicationGroup](nn-azroles-iazapplicationgroup.md) object must be submitted before it can be referenced. The destructor for an object silently discards unsubmitted changes.

## -see-also

[IAzApplicationGroup](nn-azroles-iazapplicationgroup.md)
