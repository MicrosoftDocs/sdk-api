---
UID: NF:wcmconfig.ISettingsEngine.CreateSettingsContext
title: ISettingsEngine::CreateSettingsContext (wcmconfig.h)
description: Creates a settings context.
helpviewer_keywords: ["CreateSettingsContext","CreateSettingsContext method [SMI]","CreateSettingsContext method [SMI]","ISettingsEngine interface","ISettingsEngine interface [SMI]","CreateSettingsContext method","ISettingsEngine.CreateSettingsContext","ISettingsEngine::CreateSettingsContext","smi.isettingsengine_createsettingscontext","wcmconfig/ISettingsEngine::CreateSettingsContext"]
old-location: smi\isettingsengine_createsettingscontext.htm
tech.root: SMI
ms.assetid: a9fe2c24-f696-4726-8e67-07280c8e8a3e
ms.date: 12/05/2018
ms.keywords: CreateSettingsContext, CreateSettingsContext method [SMI], CreateSettingsContext method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],CreateSettingsContext method, ISettingsEngine.CreateSettingsContext, ISettingsEngine::CreateSettingsContext, smi.isettingsengine_createsettingscontext, wcmconfig/ISettingsEngine::CreateSettingsContext
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
 - ISettingsEngine::CreateSettingsContext
 - wcmconfig/ISettingsEngine::CreateSettingsContext
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
 - ISettingsEngine.CreateSettingsContext
---

# ISettingsEngine::CreateSettingsContext


## -description

Creates a settings context.

## -parameters

### -param Flags [in]

The value of the Flags parameter may be 0, indicating "normal mode"  or 0x00000001, indicating <b>LIMITED_VALIDATION_MODE</b>. In normal mode, the settings context validates any changes made to list items against the current state of the target image. For example, if an  attempt is made to create a list element that already exists in the image, the create operation fails. In <b>LIMITED_VALIDATION_MODE</b>, contradictory data is not accepted. You cannot modify and then add a list item. However, no attempt is made to verify the changes made against the current state of the system. Only use <b>LIMITED_VALIDATION_MODE</b> when the intention is to author a context which is to be serialized. Do not specify this flag when creating a context to be used for <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-applysettingscontext">ISettingsEngine::ApplySettingsContext</a>. If used, the context may not be sufficiently validated and may fail during an application.

### -param Reserved [in]

Reserved. Must be <b>NULL</b>.

### -param SettingsContext [out]

A pointer to an <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingscontext">ISettingsContext</a> object that represents the created context.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. This method may return <b>E_OUTOFMEMORY</b> if there were insufficient resources to create the <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingscontext">ISettingsContext</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>