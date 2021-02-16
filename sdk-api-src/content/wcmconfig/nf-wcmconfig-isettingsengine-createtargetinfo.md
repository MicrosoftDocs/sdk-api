---
UID: NF:wcmconfig.ISettingsEngine.CreateTargetInfo
title: ISettingsEngine::CreateTargetInfo (wcmconfig.h)
description: Creates an empty target.
helpviewer_keywords: ["CreateTargetInfo","CreateTargetInfo method [SMI]","CreateTargetInfo method [SMI]","ISettingsEngine interface","ISettingsEngine interface [SMI]","CreateTargetInfo method","ISettingsEngine.CreateTargetInfo","ISettingsEngine::CreateTargetInfo","smi.isettingsengine_createtargetinfo","wcmconfig/ISettingsEngine::CreateTargetInfo"]
old-location: smi\isettingsengine_createtargetinfo.htm
tech.root: SMI
ms.assetid: f3d31643-c606-4fc1-96a8-cf5cb26bcf3f
ms.date: 12/05/2018
ms.keywords: CreateTargetInfo, CreateTargetInfo method [SMI], CreateTargetInfo method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],CreateTargetInfo method, ISettingsEngine.CreateTargetInfo, ISettingsEngine::CreateTargetInfo, smi.isettingsengine_createtargetinfo, wcmconfig/ISettingsEngine::CreateTargetInfo
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
 - ISettingsEngine::CreateTargetInfo
 - wcmconfig/ISettingsEngine::CreateTargetInfo
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
 - ISettingsEngine.CreateTargetInfo
---

# ISettingsEngine::CreateTargetInfo


## -description

Creates an empty target.

## -parameters

### -param Target [out]

An <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a> interface pointer to an empty target.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to create an ITargetInfo object.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>