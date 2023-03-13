---
UID: NF:mfmediaengine.IMFMediaEngineClassFactory4.CreateContentDecryptionModuleFactory
tech.root: mf
title: IMFMediaEngineClassFactory4::CreateContentDecryptionModuleFactory
ms.date: 06/30/2022
targetos: Windows
description: Creates an instance of IMFContentDecryptionModuleFactory, a class factory for Content Decryption Module (CDM) objects for a specified key system.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfmediaengine.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineClassFactory4::CreateContentDecryptionModuleFactory
f1_keywords:
 - IMFMediaEngineClassFactory4::CreateContentDecryptionModuleFactory
 - mfmediaengine/IMFMediaEngineClassFactory4::CreateContentDecryptionModuleFactory
dev_langs:
 - c++
helpviewer_keywords:
 - CreateContentDecryptionModuleFactory
---

## -description

Creating an instance of [IMFContentDecryptionModuleFactory](../mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodulefactory.md), a class factory for Content Decryption Module (CDM) objects, for a specified key system. 

## -parameters

### -param keySystem

An LPWSTR identifying the Key System for which the interface is created.

### -param riid

The IID of the **IMFContentDecryptionModuleFactory** interface to create.

### -param ppvObject

Receives a pointer to the created interface.

## -returns

Returns S_OK on success.

## -remarks

## -see-also

