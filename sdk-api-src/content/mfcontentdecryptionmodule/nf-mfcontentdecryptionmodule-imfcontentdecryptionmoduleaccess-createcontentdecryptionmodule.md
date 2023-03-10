---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleAccess.CreateContentDecryptionModule
title: IMFContentDecryptionModuleAccess::CreateContentDecryptionModule
ms.date: 08/05/2022
targetos: Windows
description: The IMFContentDecryptionModuleAccess::CreateContentDecryptionModule function creates a IMFContentDecryptionModule that represents a Content Decryption Module (CDM) for a DRM key system.
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
 - IMFContentDecryptionModuleAccess::CreateContentDecryptionModule
f1_keywords:
 - IMFContentDecryptionModuleAccess::CreateContentDecryptionModule
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleAccess::CreateContentDecryptionModule
dev_langs:
 - c++
---

## -description

Creates a [IMFContentDecryptionModule](nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule.md) that represents a Content Decryption Module (CDM) for a DRM key system.

## -parameters

### -param contentDecryptionModuleProperties

An [IPropertyStore](../propsys/nn-propsys-ipropertystore.md) object containing the properties for the CDM.

### -param contentDecryptionModule

Receives the created **IMFContentDecryptionModule** object.

## -returns

Returns S_OK on success.

## -remarks

The following properties are supported for the *contentDecryptionModuleProperties* parameter.

| Property                                      |Description
|-----------------------------------------------|---------------------------------------------------------------|
| [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](/windows/win32/medfound/mf-contentdecryptionmodule-inprivatestorepath) | A file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.|
| [MF_CONTENTDECRYPTIONMODULE_STOREPATH](/windows/win32/medfound/mf-contentdecryptionmodule-storepath) | A file path representing a storage location the Content Decryption Module (CDM) can use for initialization. The path specified with this property will also be used for content-specific data if the **MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH** property isn't set. |

## -see-also

