---
UID: NF:wcmconfig.ISettingsEngine.LoadStore
title: ISettingsEngine::LoadStore (wcmconfig.h)
description: Initializes and loads the schema store hive.
helpviewer_keywords: ["ISettingsEngine interface [SMI]","LoadStore method","ISettingsEngine.LoadStore","ISettingsEngine::LoadStore","LoadStore","LoadStore method [SMI]","LoadStore method [SMI]","ISettingsEngine interface","smi.isettingsengine_loadstore","wcmconfig/ISettingsEngine::LoadStore"]
old-location: smi\isettingsengine_loadstore.htm
tech.root: SMI
ms.assetid: dd255730-1c42-41a3-b274-e2abe53f210e
ms.date: 12/05/2018
ms.keywords: ISettingsEngine interface [SMI],LoadStore method, ISettingsEngine.LoadStore, ISettingsEngine::LoadStore, LoadStore, LoadStore method [SMI], LoadStore method [SMI],ISettingsEngine interface, smi.isettingsengine_loadstore, wcmconfig/ISettingsEngine::LoadStore
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
 - ISettingsEngine::LoadStore
 - wcmconfig/ISettingsEngine::LoadStore
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
 - ISettingsEngine.LoadStore
---

# ISettingsEngine::LoadStore


## -description

 Initializes and loads the schema store hive.

## -parameters

### -param Flags [in]

Flags must have a value 0 or have the value <b>LINK_STORE_TO_ENGINE_INSTANCE</b>. In a normal operation, loading the store is a persistent operation which affects the overall state of the system. The store is not cleaned up after the process exits. The developer must call <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-unloadstore">UnloadStore</a> to avoid a leak in the hive. A leak in the hive can cause future issues when accessing the same image.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -remarks

<div class="alert"><b>Note</b>  If the flag <b>LINK_STORE_TO_ENGINE_INSTANCE</b> is passed as an input parameter, the loaded store is considered attached to the current engine and will be unloaded when the <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a> object on which this method was called is finalized. The <b>ISettingsEngine</b> object can be finalized either by releasing all pointers to it, or by terminating the process. Developers can call <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-unloadstore">UnloadStore</a> to force the store to be unloaded early, but it is not necessary when this flag is used.</div>
<div> </div>
<div class="alert"><b>Note</b>  When using a target; that is, if you are not loading the store from the default file to the default location in the registry, you must call <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-unloadstore">UnloadStore</a> to verify that you do not lock the file.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>