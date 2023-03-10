---
UID: NF:wcmconfig.ISettingsEngine.CreateSettingsIdentity
title: ISettingsEngine::CreateSettingsIdentity (wcmconfig.h)
description: Creates an empty settings identity.
helpviewer_keywords: ["CreateSettingsIdentity","CreateSettingsIdentity method [SMI]","CreateSettingsIdentity method [SMI]","ISettingsEngine interface","ISettingsEngine interface [SMI]","CreateSettingsIdentity method","ISettingsEngine.CreateSettingsIdentity","ISettingsEngine::CreateSettingsIdentity","smi.isettingsengine_createsettingsidentity","wcmconfig/ISettingsEngine::CreateSettingsIdentity"]
old-location: smi\isettingsengine_createsettingsidentity.htm
tech.root: SMI
ms.assetid: b48e6784-5565-4809-873e-cadedce57743
ms.date: 12/05/2018
ms.keywords: CreateSettingsIdentity, CreateSettingsIdentity method [SMI], CreateSettingsIdentity method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],CreateSettingsIdentity method, ISettingsEngine.CreateSettingsIdentity, ISettingsEngine::CreateSettingsIdentity, smi.isettingsengine_createsettingsidentity, wcmconfig/ISettingsEngine::CreateSettingsIdentity
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
 - ISettingsEngine::CreateSettingsIdentity
 - wcmconfig/ISettingsEngine::CreateSettingsIdentity
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
 - ISettingsEngine.CreateSettingsIdentity
---

# ISettingsEngine::CreateSettingsIdentity


## -description

Creates an empty settings identity.

## -parameters

### -param SettingsID [out]

A value that returns a pointer to an empty <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsIdentity</a> object.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to allocate the <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsIdentity</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>