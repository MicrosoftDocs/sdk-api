---
UID: NF:wcmconfig.ISettingsEngine.SetTargetInfo
title: ISettingsEngine::SetTargetInfo (wcmconfig.h)
description: Sets the current offline target for the engine.
helpviewer_keywords: ["ISettingsEngine interface [SMI]","SetTargetInfo method","ISettingsEngine.SetTargetInfo","ISettingsEngine::SetTargetInfo","SetTargetInfo","SetTargetInfo method [SMI]","SetTargetInfo method [SMI]","ISettingsEngine interface","smi.isettingsengine_settargetinfo","wcmconfig/ISettingsEngine::SetTargetInfo"]
old-location: smi\isettingsengine_settargetinfo.htm
tech.root: SMI
ms.assetid: a33a0155-0533-4450-9e03-2688ad776a1a
ms.date: 12/05/2018
ms.keywords: ISettingsEngine interface [SMI],SetTargetInfo method, ISettingsEngine.SetTargetInfo, ISettingsEngine::SetTargetInfo, SetTargetInfo, SetTargetInfo method [SMI], SetTargetInfo method [SMI],ISettingsEngine interface, smi.isettingsengine_settargetinfo, wcmconfig/ISettingsEngine::SetTargetInfo
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
 - ISettingsEngine::SetTargetInfo
 - wcmconfig/ISettingsEngine::SetTargetInfo
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
 - ISettingsEngine.SetTargetInfo
---

# ISettingsEngine::SetTargetInfo


## -description

Sets the current offline target for the engine.

## -parameters

### -param Target [in]

An <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a> value that specifies the target.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>