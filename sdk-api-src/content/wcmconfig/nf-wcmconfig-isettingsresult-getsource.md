---
UID: NF:wcmconfig.ISettingsResult.GetSource
title: ISettingsResult::GetSource (wcmconfig.h)
description: Returns the file or path where the error has occurred.
helpviewer_keywords: ["GetSource","GetSource method [SMI]","GetSource method [SMI]","ISettingsResult interface","ISettingsResult interface [SMI]","GetSource method","ISettingsResult.GetSource","ISettingsResult::GetSource","smi.isettingsresult_getsource","wcmconfig/ISettingsResult::GetSource"]
old-location: smi\isettingsresult_getsource.htm
tech.root: SMI
ms.assetid: 2a76b243-5294-47a7-8ad3-b39425735866
ms.date: 12/05/2018
ms.keywords: GetSource, GetSource method [SMI], GetSource method [SMI],ISettingsResult interface, ISettingsResult interface [SMI],GetSource method, ISettingsResult.GetSource, ISettingsResult::GetSource, smi.isettingsresult_getsource, wcmconfig/ISettingsResult::GetSource
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
 - ISettingsResult::GetSource
 - wcmconfig/ISettingsResult::GetSource
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
 - ISettingsResult.GetSource
---

# ISettingsResult::GetSource


## -description

Returns the file or path where the error has occurred.

## -parameters

### -param file [out]

The file or path where the error has occurred.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsresult">ISettingsResult</a>