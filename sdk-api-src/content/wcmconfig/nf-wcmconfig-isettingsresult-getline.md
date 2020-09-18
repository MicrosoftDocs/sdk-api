---
UID: NF:wcmconfig.ISettingsResult.GetLine
title: ISettingsResult::GetLine (wcmconfig.h)
description: Returns the line number where the error has occurred.
helpviewer_keywords: ["GetLine","GetLine method [SMI]","GetLine method [SMI]","ISettingsResult interface","ISettingsResult interface [SMI]","GetLine method","ISettingsResult.GetLine","ISettingsResult::GetLine","smi.isettingsresult_getline","wcmconfig/ISettingsResult::GetLine"]
old-location: smi\isettingsresult_getline.htm
tech.root: SMI
ms.assetid: c74beea9-5e81-4cd2-ade2-c812b6a035a1
ms.date: 12/05/2018
ms.keywords: GetLine, GetLine method [SMI], GetLine method [SMI],ISettingsResult interface, ISettingsResult interface [SMI],GetLine method, ISettingsResult.GetLine, ISettingsResult::GetLine, smi.isettingsresult_getline, wcmconfig/ISettingsResult::GetLine
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
 - ISettingsResult::GetLine
 - wcmconfig/ISettingsResult::GetLine
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
 - ISettingsResult.GetLine
---

# ISettingsResult::GetLine


## -description

Returns the line number where the error has occurred.

## -parameters

### -param dwLine [out]

The line number where the error has occurred.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsresult">ISettingsResult</a>