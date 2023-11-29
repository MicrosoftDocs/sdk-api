---
UID: NF:sspi.QueryCredentialsAttributesExA
tech.root: security
title: QueryCredentialsAttributesExA
ms.date: 07/20/2022
targetos: Windows
description: Query the attributes of a security context.
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
 - QueryCredentialsAttributesExA
 - QueryCredentialsAttributesEx
f1_keywords:
 - QueryCredentialsAttributesExA
 - sspi/QueryCredentialsAttributesExA
 - QueryCredentialsAttributesEx
 - sspi/QueryCredentialsAttributesEx
dev_langs:
 - c++
helpviewer_keywords:
 - QueryCredentialsAttributesExA
---

## -description

Query the attributes of a security context.

## -parameters

### -param phCredential

The credential to query.

### -param ulAttribute

The attribute to query.

### -param pBuffer

The buffer to receive the attributes.

### -param cbBuffer

The length of the buffer.

## -returns

Returns **TRUE** if the function succeeds, **FALSE** otherwise.

## -remarks

## -see-also
