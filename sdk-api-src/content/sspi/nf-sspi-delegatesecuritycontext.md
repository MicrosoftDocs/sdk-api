---
UID: NF:sspi.DelegateSecurityContext
tech.root: security
title: DelegateSecurityContext
ms.date: 07/20/2022
targetos: Windows
description: Delegates the security context to the specified server.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - DelegateSecurityContext
f1_keywords:
 - DelegateSecurityContext
 - sspi/DelegateSecurityContext
dev_langs:
 - c++
helpviewer_keywords:
 - DelegateSecurityContext
---

## -description

Delegates the security context to the specified server.

## -parameters

### -param phContext

The security context to delegate.

### -param pTarget

The target path.

### -param DelegationType

The type of delegation.

### -param pExpiry

The **optional** time limit, after which the context expires.

### -param pPackageParameters

The **optional** package-specific parameters.

### -param pOutput

The output token for [ApplyControlToken](nf-sspi-applycontroltoken.md).

## -returns

Returns a value indicating the result of the operation.

## -remarks

## -see-also

[ApplyControlToken](nf-sspi-applycontroltoken.md)
