---
UID: NF:wcmconfig.ISettingsEngine.GetTargetInfo
title: ISettingsEngine::GetTargetInfo (wcmconfig.h)
description: Gets the current offline target for the engine.
helpviewer_keywords: ["GetTargetInfo","GetTargetInfo method [SMI]","GetTargetInfo method [SMI]","ISettingsEngine interface","ISettingsEngine interface [SMI]","GetTargetInfo method","ISettingsEngine.GetTargetInfo","ISettingsEngine::GetTargetInfo","smi.isettingsengine_gettargetinfo","wcmconfig/ISettingsEngine::GetTargetInfo"]
old-location: smi\isettingsengine_gettargetinfo.htm
tech.root: SMI
ms.assetid: 2e14644b-84bc-48eb-8d8c-d6290db72dea
ms.date: 12/05/2018
ms.keywords: GetTargetInfo, GetTargetInfo method [SMI], GetTargetInfo method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],GetTargetInfo method, ISettingsEngine.GetTargetInfo, ISettingsEngine::GetTargetInfo, smi.isettingsengine_gettargetinfo, wcmconfig/ISettingsEngine::GetTargetInfo
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
 - ISettingsEngine::GetTargetInfo
 - wcmconfig/ISettingsEngine::GetTargetInfo
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
 - ISettingsEngine.GetTargetInfo
---

# ISettingsEngine::GetTargetInfo


## -description

Gets the current offline target for the engine.

## -parameters

### -param Target [out]

A pointer to an <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a> object that is the current target for the engine.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>