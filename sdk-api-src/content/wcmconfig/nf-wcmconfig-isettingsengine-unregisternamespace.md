---
UID: NF:wcmconfig.ISettingsEngine.UnregisterNamespace
title: ISettingsEngine::UnregisterNamespace (wcmconfig.h)
description: Unregisters an existing namespace.
helpviewer_keywords: ["ISettingsEngine interface [SMI]","UnregisterNamespace method","ISettingsEngine.UnregisterNamespace","ISettingsEngine::UnregisterNamespace","UnregisterNamespace","UnregisterNamespace method [SMI]","UnregisterNamespace method [SMI]","ISettingsEngine interface","smi.isettingsengine_unregisternamespace","wcmconfig/ISettingsEngine::UnregisterNamespace"]
old-location: smi\isettingsengine_unregisternamespace.htm
tech.root: SMI
ms.assetid: c7254f87-fdf8-4b51-9a06-e593490cd3c5
ms.date: 12/05/2018
ms.keywords: ISettingsEngine interface [SMI],UnregisterNamespace method, ISettingsEngine.UnregisterNamespace, ISettingsEngine::UnregisterNamespace, UnregisterNamespace, UnregisterNamespace method [SMI], UnregisterNamespace method [SMI],ISettingsEngine interface, smi.isettingsengine_unregisternamespace, wcmconfig/ISettingsEngine::UnregisterNamespace
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
 - ISettingsEngine::UnregisterNamespace
 - wcmconfig/ISettingsEngine::UnregisterNamespace
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
 - ISettingsEngine.UnregisterNamespace
---

# ISettingsEngine::UnregisterNamespace


## -description

Unregisters an existing namespace. This method is deprecated.

## -parameters

### -param SettingsID [in]

An <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsidentity">ISettingsIdentity</a> interface value that identifies the namespace to be unregistered.

### -param RemoveSettings [in]

When <b>true</b>, specifies that settings must be removed.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>