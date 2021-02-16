---
UID: NF:wcmconfig.ITargetInfo.LoadModule
title: ITargetInfo::LoadModule (wcmconfig.h)
description: Loads the module from the offline installation location.
helpviewer_keywords: ["ITargetInfo interface [SMI]","LoadModule method","ITargetInfo.LoadModule","ITargetInfo::LoadModule","LoadModule","LoadModule method [SMI]","LoadModule method [SMI]","ITargetInfo interface","smi.itargetinfo_loadmodule","wcmconfig/ITargetInfo::LoadModule"]
old-location: smi\itargetinfo_loadmodule.htm
tech.root: SMI
ms.assetid: 863aefc6-d777-4af9-b310-adadef993bcd
ms.date: 12/05/2018
ms.keywords: ITargetInfo interface [SMI],LoadModule method, ITargetInfo.LoadModule, ITargetInfo::LoadModule, LoadModule, LoadModule method [SMI], LoadModule method [SMI],ITargetInfo interface, smi.itargetinfo_loadmodule, wcmconfig/ITargetInfo::LoadModule
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
 - ITargetInfo::LoadModule
 - wcmconfig/ITargetInfo::LoadModule
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
 - ITargetInfo.LoadModule
---

# ITargetInfo::LoadModule


## -description

Loads the module from the offline installation location.

## -parameters

### -param Module [in]

The name of the module.

### -param ModuleHandle [out]

The module handle.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>