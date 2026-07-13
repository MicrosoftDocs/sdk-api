---
UID: NF:wincrypt.CryptGetAsyncParam
title: CryptGetAsyncParam
description: The CryptGetAsyncParam function (wincrypt.h) sets an async parameter value.
ms.date: 08/03/2022
ms.keywords: CryptGetAsyncParam
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
 - CryptGetAsyncParam
 - wincrypt/CryptGetAsyncParam
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - secforwarder.dll
api_name:
 - CryptGetAsyncParam
---

## -description

Sets an async parameter value.

## -parameters

### -param hAsync

An async handle.

### -param pszParamOid

The parameter ID.

### -param ppvParam

Receives the parameter value.

### -param ppfnFree

A callback function called when the parameter is freed.

## -returns

S_OK on success.

## -remarks

## -see-also

