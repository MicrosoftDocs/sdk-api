---
UID: NF:wcmconfig.ISettingsEngine.RegisterNamespace
title: ISettingsEngine::RegisterNamespace (wcmconfig.h)
description: Registers a namespace from a stream.
helpviewer_keywords: ["ISettingsEngine interface [SMI]","RegisterNamespace method","ISettingsEngine.RegisterNamespace","ISettingsEngine::RegisterNamespace","RegisterNamespace","RegisterNamespace method [SMI]","RegisterNamespace method [SMI]","ISettingsEngine interface","smi.isettingsengine_registernamespace","wcmconfig/ISettingsEngine::RegisterNamespace"]
old-location: smi\isettingsengine_registernamespace.htm
tech.root: SMI
ms.assetid: 9b9ffba8-b2b7-469e-96d2-78b086987fae
ms.date: 12/05/2018
ms.keywords: ISettingsEngine interface [SMI],RegisterNamespace method, ISettingsEngine.RegisterNamespace, ISettingsEngine::RegisterNamespace, RegisterNamespace, RegisterNamespace method [SMI], RegisterNamespace method [SMI],ISettingsEngine interface, smi.isettingsengine_registernamespace, wcmconfig/ISettingsEngine::RegisterNamespace
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISettingsEngine::RegisterNamespace
 - wcmconfig/ISettingsEngine::RegisterNamespace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsEngine.RegisterNamespace
---

# ISettingsEngine::RegisterNamespace


## -description

Registers a namespace from a stream. The stream passed as a parameter to this method must be the XML for the configuration section of a manifest. This method is deprecated.

## -parameters

### -param SettingsID [in]

An <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsidentity">ISettingsIdentity</a> value that identifies the namespace to be registered.

### -param Stream [in]

The stream that specifies the configuration.

### -param PushSettings [in]

When this flag is set to <b>TRUE</b>, settings are pushed to the registry or to the initialization files. If the flag is not set, only the store for settings is changed.

### -param Results [out]

Results is a variant of type <b>VT_VARIANT</b> or <b>VT_ARRAY</b>, each of which points to an <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsresult">ISettingsResult</a> object which describes an error or warning uncovered during manifest compilation.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>