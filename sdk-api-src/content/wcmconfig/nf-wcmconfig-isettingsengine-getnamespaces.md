---
UID: NF:wcmconfig.ISettingsEngine.GetNamespaces
title: ISettingsEngine::GetNamespaces (wcmconfig.h)
description: Returns an enumerator to the installed namespaces.
helpviewer_keywords: ["GetNamespaces","GetNamespaces method [SMI]","GetNamespaces method [SMI]","ISettingsEngine interface","ISettingsEngine interface [SMI]","GetNamespaces method","ISettingsEngine.GetNamespaces","ISettingsEngine::GetNamespaces","smi.isettingsengine_getnamespaces","wcmconfig/ISettingsEngine::GetNamespaces"]
old-location: smi\isettingsengine_getnamespaces.htm
tech.root: SMI
ms.assetid: 0beb20a5-3dbf-48c8-9b0c-aa3dd094b59d
ms.date: 12/05/2018
ms.keywords: GetNamespaces, GetNamespaces method [SMI], GetNamespaces method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],GetNamespaces method, ISettingsEngine.GetNamespaces, ISettingsEngine::GetNamespaces, smi.isettingsengine_getnamespaces, wcmconfig/ISettingsEngine::GetNamespaces
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
 - ISettingsEngine::GetNamespaces
 - wcmconfig/ISettingsEngine::GetNamespaces
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
 - ISettingsEngine.GetNamespaces
---

# ISettingsEngine::GetNamespaces


## -description

Returns an enumerator to the installed namespaces.

## -parameters

### -param Flags [in]

A <a href="/windows/win32/api/wcmconfig/ne-wcmconfig-wcmnamespaceenumerationflags">WcmNamespaceEnumerationFlags</a> value that specifies the context to include in the collection of namespaces.

### -param Reserved [in]

Reserved. Must be <b>NULL</b>.

### -param Namespaces [out]

An <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-iitemenumerator">IItemEnumerator</a> interface pointer whose methods can be used to access members of the collection.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_USERNOTFOUND</b> if the store is not loaded.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>