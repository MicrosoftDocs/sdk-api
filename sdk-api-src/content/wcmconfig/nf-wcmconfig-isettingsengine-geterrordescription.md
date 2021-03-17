---
UID: NF:wcmconfig.ISettingsEngine.GetErrorDescription
title: ISettingsEngine::GetErrorDescription (wcmconfig.h)
description: Retrieves a text message for a returned HRESULT code.
helpviewer_keywords: ["GetErrorDescription","GetErrorDescription method [SMI]","GetErrorDescription method [SMI]","ISettingsEngine interface","ISettingsEngine interface [SMI]","GetErrorDescription method","ISettingsEngine.GetErrorDescription","ISettingsEngine::GetErrorDescription","smi.isettingsengine_geterrordescription","wcmconfig/ISettingsEngine::GetErrorDescription"]
old-location: smi\isettingsengine_geterrordescription.htm
tech.root: SMI
ms.assetid: 1a1ac3eb-c2d5-4a23-928e-51ef1a52ad73
ms.date: 12/05/2018
ms.keywords: GetErrorDescription, GetErrorDescription method [SMI], GetErrorDescription method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],GetErrorDescription method, ISettingsEngine.GetErrorDescription, ISettingsEngine::GetErrorDescription, smi.isettingsengine_geterrordescription, wcmconfig/ISettingsEngine::GetErrorDescription
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
 - ISettingsEngine::GetErrorDescription
 - wcmconfig/ISettingsEngine::GetErrorDescription
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
 - ISettingsEngine.GetErrorDescription
---

# ISettingsEngine::GetErrorDescription


## -description

Retrieves a text message for a returned HRESULT code.

## -parameters

### -param HResult [in]

The HRESULT code for which this method retrieves the error description.

### -param Message [out]

The text message that corresponds to the HRESULT code.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to allocate the string returned in the message.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>