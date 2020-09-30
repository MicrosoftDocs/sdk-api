---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleFactory.IsTypeSupported
title: IMFContentDecryptionModuleFactory::IsTypeSupported
ms.date: 11/26/2019
ms.topic: language-reference
targetos: Windows
description: Queries whether the specified Key System and, optionally, content type are supported.
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
 - IMFContentDecryptionModuleFactory::IsTypeSupported
f1_keywords:
 - IMFContentDecryptionModuleFactory::IsTypeSupported
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleFactory::IsTypeSupported
dev_langs:
 - c++
---

## -description

Queries whether the specified Key System and, optionally, content type are supported.

## -parameters

### -param keySystem

An **LPCWSTR** specifying the Key System for which support is being queried.

### -param contentType

Optional. An **LPCWSTR** specifying the content type for which support is being queried.

## -returns

True if the specified Key System and content type are supported; otherwise, false.

## -remarks

For information about Key Systems, see the Encrypted Media Extension specification's [Key System](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#key-system)

## -see-also

