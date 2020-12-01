---
UID: NF:wcmconfig.ISettingsNamespace.Settings
title: ISettingsNamespace::Settings (wcmconfig.h)
description: Retrieves an enumerator for the top-level settings for the namespace.
helpviewer_keywords: ["ISettingsNamespace interface [SMI]","Settings method","ISettingsNamespace.Settings","ISettingsNamespace::Settings","Settings","Settings method [SMI]","Settings method [SMI]","ISettingsNamespace interface","smi.isettingsnamespace_settings","wcmconfig/ISettingsNamespace::Settings"]
old-location: smi\isettingsnamespace_settings.htm
tech.root: SMI
ms.assetid: 86ec9224-5704-4a7d-b554-f9baf3f14531
ms.date: 12/05/2018
ms.keywords: ISettingsNamespace interface [SMI],Settings method, ISettingsNamespace.Settings, ISettingsNamespace::Settings, Settings, Settings method [SMI], Settings method [SMI],ISettingsNamespace interface, smi.isettingsnamespace_settings, wcmconfig/ISettingsNamespace::Settings
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
 - ISettingsNamespace::Settings
 - wcmconfig/ISettingsNamespace::Settings
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
 - ISettingsNamespace.Settings
---

# ISettingsNamespace::Settings


## -description

Retrieves an enumerator for the top-level settings for the namespace.

## -parameters

### -param Settings [out]

A pointer to an  <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-iitemenumerator">IItemEnumerator</a> object that provides methods to access all the settings for this namespace.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsnamespace">ISettingsNamespace</a>