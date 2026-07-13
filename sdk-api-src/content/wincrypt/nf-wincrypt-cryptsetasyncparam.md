---
UID: NF:wincrypt.CryptSetAsyncParam
title: CryptSetAsyncParam
description: The CryptSetAsyncParam function (wincrypt.h) sets an async parameter.
ms.date: 08/03/2022
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
req.lib: Crypt32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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

The parameter value.

### -param pfnFree

A callback function called when the parameter is freed.

## -returns

S_OK on success.

## -remarks

## -see-also

