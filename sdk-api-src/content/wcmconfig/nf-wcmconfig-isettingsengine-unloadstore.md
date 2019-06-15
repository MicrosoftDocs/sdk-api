---
UID: NF:wcmconfig.ISettingsEngine.UnloadStore
title: ISettingsEngine::UnloadStore (wcmconfig.h)
author: windows-sdk-content
description: Unloads the schema store hive and frees resources.
old-location: smi\isettingsengine_unloadstore.htm
tech.root: SMI
ms.assetid: 10c0e5c7-41df-4ebb-86be-0c2c6e013849
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISettingsEngine interface [SMI],UnloadStore method, ISettingsEngine.UnloadStore, ISettingsEngine::UnloadStore, UnloadStore, UnloadStore method [SMI], UnloadStore method [SMI],ISettingsEngine interface, smi.isettingsengine_unloadstore, wcmconfig/ISettingsEngine::UnloadStore
ms.topic: method
f1_keywords: ["wcmconfig/ISettingsEngine.UnloadStore"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsEngine.UnloadStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISettingsEngine::UnloadStore


## -description


 Unloads the schema store hive and frees resources.   If there are currently unreleased SMI objects when calling this method, it fails and returns an error value <b>E_ACCESSDENIED</b>. You must release all SMI objects before calling <b>UnloadStore</b>.


## -parameters




### -param Reserved [in]

Reserved.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. If there are currently unreleased SMI objects when calling <b>UnloadStore</b>, <b>UnloadStore</b> will fail and return <b>E_ACCESSDENIED</b>. Before calling <b>UnloadStore</b>, release all SMI objects. If the store was not already loaded, it may return <b>E_INVALIDARG</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>
 

 

