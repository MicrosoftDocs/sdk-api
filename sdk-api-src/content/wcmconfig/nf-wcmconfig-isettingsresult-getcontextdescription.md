---
UID: NF:wcmconfig.ISettingsResult.GetContextDescription
title: ISettingsResult::GetContextDescription (wcmconfig.h)
description: Returns the description of the context that surrounds the error.
helpviewer_keywords: ["GetContextDescription","GetContextDescription method [SMI]","GetContextDescription method [SMI]","ISettingsResult interface","ISettingsResult interface [SMI]","GetContextDescription method","ISettingsResult.GetContextDescription","ISettingsResult::GetContextDescription","smi.isettingsresult_getcontextdescription","wcmconfig/ISettingsResult::GetContextDescription"]
old-location: smi\isettingsresult_getcontextdescription.htm
tech.root: SMI
ms.assetid: d2bb39ce-9c49-46ab-b7d7-e4e4794f6b5a
ms.date: 12/05/2018
ms.keywords: GetContextDescription, GetContextDescription method [SMI], GetContextDescription method [SMI],ISettingsResult interface, ISettingsResult interface [SMI],GetContextDescription method, ISettingsResult.GetContextDescription, ISettingsResult::GetContextDescription, smi.isettingsresult_getcontextdescription, wcmconfig/ISettingsResult::GetContextDescription
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
 - ISettingsResult::GetContextDescription
 - wcmconfig/ISettingsResult::GetContextDescription
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
 - ISettingsResult.GetContextDescription
---

# ISettingsResult::GetContextDescription


## -description

Returns the description of the context that surrounds the error.

## -parameters

### -param description [out]

The text that describes the context.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsresult">ISettingsResult</a>