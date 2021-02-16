---
UID: NF:comsvcs.IServiceSxsConfig.SxsConfig
title: IServiceSxsConfig::SxsConfig (comsvcs.h)
description: Configures the side-by-side assembly for the enclosed work.
helpviewer_keywords: ["IServiceSxsConfig interface [COM+]","SxsConfig method","IServiceSxsConfig.SxsConfig","IServiceSxsConfig::SxsConfig","SxsConfig","SxsConfig method [COM+]","SxsConfig method [COM+]","IServiceSxsConfig interface","_cos_IServiceSxsConfig_SxsConfig","comsvcs/IServiceSxsConfig::SxsConfig","cos.iservicesxsconfig_sxsconfig"]
old-location: cos\iservicesxsconfig_sxsconfig.htm
tech.root: cos
ms.assetid: ce067aca-8bb4-48ac-b466-9080d2166bdd
ms.date: 12/05/2018
ms.keywords: IServiceSxsConfig interface [COM+],SxsConfig method, IServiceSxsConfig.SxsConfig, IServiceSxsConfig::SxsConfig, SxsConfig, SxsConfig method [COM+], SxsConfig method [COM+],IServiceSxsConfig interface, _cos_IServiceSxsConfig_SxsConfig, comsvcs/IServiceSxsConfig::SxsConfig, cos.iservicesxsconfig_sxsconfig
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IServiceSxsConfig::SxsConfig
 - comsvcs/IServiceSxsConfig::SxsConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServiceSxsConfig.SxsConfig
---

# IServiceSxsConfig::SxsConfig


## -description

Configures the side-by-side assembly for the enclosed work.

## -parameters

### -param scsConfig [in]

A value from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_sxsconfig">CSC_SxsConfig</a> enumeration.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

The <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicesxsconfig-sxsdirectory">SxsDirectory</a> method must be called if a new side-by-side assembly domain is created using a call to this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicesxsconfig">IServiceSxsConfig</a>