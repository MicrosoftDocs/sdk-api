---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleAccess.GetConfiguration
title: IMFContentDecryptionModuleAccess::GetConfiguration
ms.date: 11/26/2019
targetos: Windows
description: Returns the supported combination of configuration options.
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
 - IMFContentDecryptionModuleAccess::GetConfiguration
f1_keywords:
 - IMFContentDecryptionModuleAccess::GetConfiguration
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleAccess::GetConfiguration
dev_langs:
 - c++
---

## -description

Returns the supported combination of configuration options.

## -parameters

### -param configuration

Receives a reference to an [IPropertyStore](../propsys/nn-propsys-ipropertystore.md) object containing the configuration options for the CDM.

## -returns

Returns S_OK on success.

## -remarks

**GetConfiguration** is based on the Encrypted Media Extension specification's [MediaKeySystemAccess.keySystem](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeysystemaccess-getconfiguration).

## -see-also