---
UID: NF:comppkgsup.GetDefaultContentDecryptionModuleFactory
tech.root: winprog
title: GetDefaultContentDecryptionModuleFactory
ms.date: 02/15/2024
targetos: Windows
description: Returns the implementation of IMFContentDecryptionModuleFactory for the specified key system that is built-in to Windows.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Comppkgsup.dll
req.header: comppkgsup.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Comppkgsup.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 24H2
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
 - comppkgsup.h
api_name:
 - GetDefaultContentDecryptionModuleFactory
f1_keywords:
 - GetDefaultContentDecryptionModuleFactory
 - comppkgsup/GetDefaultContentDecryptionModuleFactory
dev_langs:
 - c++
helpviewer_keywords:
 - GetDefaultContentDecryptionModuleFactory
---

## -description

Returns the implementation of [IMFContentDecryptionModuleFactory](../mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodulefactory.md) for the specified key system that is built-in to Windows.

## -parameters

### -param keySystem [in]

A PCWSTR identifying the key system for which the decryption module is returned.

### -param contentDecryptionModuleFactory [out]

If the specified key system is found, receives pointer to an **IMFContentDecryptionModuleFactory** implementation; otherwise, NULL.

## -returns

An HRESULT including the following values:

| Value | Description |
|-------|-------------|
| S_OK  | Success. This function returns success even if the specified key system is not found, but in this case, the *contentDecryptionModuleFactory* parameter is NULL.   |
| CO_E_NOTINITIALIZED | COM was not initialized before the function was called |


## -remarks

**GetDefaultContentDescryptionModuleFactory** only considers content decryption module factories that are built-in to Windows and does not consider content decryption module factories that have been downloaded from the Microsoft Store. 

It is recommended that apps use [IMFMediaEngineClassFactory4::CreateContentDecryptionModuleFactory](../windows/win32/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory4-createcontentdecryptionmodulefactory), as this method first calls **GetDefaultContentDecryptionModuleFactory** , but then also searches for any matching implementations of **IMFContentDecryptionModuleFactory** that may have been downloaded from the Microsoft Store.

## -see-also

