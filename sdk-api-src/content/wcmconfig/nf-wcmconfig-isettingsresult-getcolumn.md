---
UID: NF:wcmconfig.ISettingsResult.GetColumn
title: ISettingsResult::GetColumn (wcmconfig.h)
description: Returns the column number where the error occurred.
helpviewer_keywords: ["GetColumn","GetColumn method [SMI]","GetColumn method [SMI]","ISettingsResult interface","ISettingsResult interface [SMI]","GetColumn method","ISettingsResult.GetColumn","ISettingsResult::GetColumn","smi.isettingsresult_getcolumn","wcmconfig/ISettingsResult::GetColumn"]
old-location: smi\isettingsresult_getcolumn.htm
tech.root: SMI
ms.assetid: 09e1c5ae-f5ba-4f5a-b35d-a1c2e8dbdfe9
ms.date: 12/05/2018
ms.keywords: GetColumn, GetColumn method [SMI], GetColumn method [SMI],ISettingsResult interface, ISettingsResult interface [SMI],GetColumn method, ISettingsResult.GetColumn, ISettingsResult::GetColumn, smi.isettingsresult_getcolumn, wcmconfig/ISettingsResult::GetColumn
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
 - ISettingsResult::GetColumn
 - wcmconfig/ISettingsResult::GetColumn
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
 - ISettingsResult.GetColumn
---

# ISettingsResult::GetColumn


## -description

Returns the column number where the error occurred.

## -parameters

### -param dwColumn [out]

The column which is the source of the error.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsresult">ISettingsResult</a>