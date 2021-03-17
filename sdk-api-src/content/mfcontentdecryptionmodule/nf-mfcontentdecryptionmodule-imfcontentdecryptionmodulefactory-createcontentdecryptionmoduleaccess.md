---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleFactory.CreateContentDecryptionModuleAccess
title: IMFContentDecryptionModuleFactory::CreateContentDecryptionModuleAccess
ms.date: 11/26/2019
targetos: Windows
description: Creates an instance of the IMFContentDecryptionModuleAccess interface.
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
 - IMFContentDecryptionModuleFactory::CreateContentDecryptionModuleAccess
f1_keywords:
 - IMFContentDecryptionModuleFactory::CreateContentDecryptionModuleAccess
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleFactory::CreateContentDecryptionModuleAccess
dev_langs:
 - c++
---

## -description

Creates an instance of the [IMFContentDecryptionModuleAccess](nn-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess.md) interface.

## -parameters

### -param keySystem

An **LPWSTR** identifying the Key System for which the interface is created.

### -param configurations

An [IPropertyStore](../propsys/nn-propsys-ipropertystore.md) object containing the configuration options for the CDM.

### -param numConfigurations

A **DWORD** specifying the number of properties in the *configurations* parameter.

### -param contentDecryptionModuleAccess

Receives the created **IMFContentDecryptionModuleAccess** object.

## -returns

Returns S_OK on success.

## -remarks

**IMFContentDecryptionModuleAccess** is based on the Encrypted Media Extension specification's [MediaKeySystemAccess.getConfiguration](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#mediakeysystemaccess-interface).

## -see-also

- [IMFContentDecryptionModuleAccess](nn-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess.md)