---
UID: NF:wincrypt.CryptSetAsyncParam
title: CryptSetAsyncParam
ms.date: 4/26/2019
ms.keywords: CryptSetAsyncParam
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wincrypt.h
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
f1_keywords:
 - CryptSetAsyncParam
 - wincrypt/CryptSetAsyncParam
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - 
api_location:
 - wincrypt.h
api_name:
 - CryptSetAsyncParam
---

## -description

Sets an async parameter.

## -parameters

### -param hAsync

An async handle.

### -param pszParamOid

The parameter ID.

### -param pvParam

The paramter value.

### -param pfnFree

A callback function called when the parameter is freed.

## -returns

S_OK on success.

## -remarks

## -see-also

