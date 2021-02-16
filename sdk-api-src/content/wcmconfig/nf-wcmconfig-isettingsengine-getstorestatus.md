---
UID: NF:wcmconfig.ISettingsEngine.GetStoreStatus
title: ISettingsEngine::GetStoreStatus (wcmconfig.h)
description: Gets the status of the schema store.
helpviewer_keywords: ["GetStoreStatus","GetStoreStatus method [SMI]","GetStoreStatus method [SMI]","ISettingsEngine interface","ISettingsEngine interface [SMI]","GetStoreStatus method","ISettingsEngine.GetStoreStatus","ISettingsEngine::GetStoreStatus","smi.isettingsengine_getstorestatus","wcmconfig/ISettingsEngine::GetStoreStatus"]
old-location: smi\isettingsengine_getstorestatus.htm
tech.root: SMI
ms.assetid: 212299b4-d7b3-4a11-b75e-7e752bb91932
ms.date: 12/05/2018
ms.keywords: GetStoreStatus, GetStoreStatus method [SMI], GetStoreStatus method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],GetStoreStatus method, ISettingsEngine.GetStoreStatus, ISettingsEngine::GetStoreStatus, smi.isettingsengine_getstorestatus, wcmconfig/ISettingsEngine::GetStoreStatus
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
 - ISettingsEngine::GetStoreStatus
 - wcmconfig/ISettingsEngine::GetStoreStatus
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
 - ISettingsEngine.GetStoreStatus
---

# ISettingsEngine::GetStoreStatus


## -description

Gets the status of the schema store.

## -parameters

### -param Reserved [in]

Reserved. Must be <b>NULL</b>.

### -param Status [out]

A <a href="/windows/win32/api/wcmconfig/ne-wcmconfig-wcmuserstatus">WcmUserStatus</a> value that indicates the status of the store.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>