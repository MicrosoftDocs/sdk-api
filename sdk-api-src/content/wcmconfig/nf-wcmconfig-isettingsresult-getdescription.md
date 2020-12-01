---
UID: NF:wcmconfig.ISettingsResult.GetDescription
title: ISettingsResult::GetDescription (wcmconfig.h)
description: Returns the description of the error.
helpviewer_keywords: ["GetDescription","GetDescription method [SMI]","GetDescription method [SMI]","ISettingsResult interface","ISettingsResult interface [SMI]","GetDescription method","ISettingsResult.GetDescription","ISettingsResult::GetDescription","smi.isettingsresult_getdescription","wcmconfig/ISettingsResult::GetDescription"]
old-location: smi\isettingsresult_getdescription.htm
tech.root: SMI
ms.assetid: d020bd46-8967-4105-856d-ee448b527852
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [SMI], GetDescription method [SMI],ISettingsResult interface, ISettingsResult interface [SMI],GetDescription method, ISettingsResult.GetDescription, ISettingsResult::GetDescription, smi.isettingsresult_getdescription, wcmconfig/ISettingsResult::GetDescription
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
 - ISettingsResult::GetDescription
 - wcmconfig/ISettingsResult::GetDescription
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
 - ISettingsResult.GetDescription
---

# ISettingsResult::GetDescription


## -description

Returns the description of the error.

## -parameters

### -param description [out]

The text that describes the error.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsresult">ISettingsResult</a>