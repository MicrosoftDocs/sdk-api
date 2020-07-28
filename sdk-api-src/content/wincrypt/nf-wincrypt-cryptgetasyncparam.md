---
UID: NF:wincrypt.CryptGetAsyncParam
title: CryptGetAsyncParam
ms.date: 4/26/2019
ms.keywords: CryptGetAsyncParam
f1_keywords:
- CryptGetAsyncParam
dev_langs:
- c++
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

