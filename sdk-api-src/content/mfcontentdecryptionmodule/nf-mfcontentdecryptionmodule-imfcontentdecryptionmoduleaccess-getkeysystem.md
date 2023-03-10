---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleAccess.GetKeySystem
title: IMFContentDecryptionModuleAccess::GetKeySystem
ms.date: 11/26/2019
targetos: Windows
description: Gets a string identifying the Key System being used by the Content Decryption Module (CDM).
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfcontentdecryptionmodule.h
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
 - mfcontentdecryptionmodule.h
api_name:
 - IMFContentDecryptionModuleAccess::GetKeySystem
f1_keywords:
 - IMFContentDecryptionModuleAccess::GetKeySystem
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleAccess::GetKeySystem
dev_langs:
 - c++
---

## -description

Gets a string identifying the Key System being used by the Content Decryption Module (CDM).

## -parameters

### -param keySystem

Receives a pointer to an **LPWSTR** identifying the Key System.

## -returns

Returns S_OK on success.

## -remarks

The *keySystem* memory must be allocated and freed using [CoTaskMem](../combaseapi/nf-combaseapi-cotaskmemalloc.md).

**GetKeySystem** is based on the Encrypted Media Extension specification's [MediaKeySystemAccess.getConfiguration](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeysystemaccess-keysystem).

## -see-also