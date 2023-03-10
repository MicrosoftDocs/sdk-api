---
UID: NF:comsvcs.IServiceSxsConfig.SxsDirectory
title: IServiceSxsConfig::SxsDirectory (comsvcs.h)
description: Sets the directory for the side-by-side assembly for the enclosed work.
helpviewer_keywords: ["IServiceSxsConfig interface [COM+]","SxsDirectory method","IServiceSxsConfig.SxsDirectory","IServiceSxsConfig::SxsDirectory","SxsDirectory","SxsDirectory method [COM+]","SxsDirectory method [COM+]","IServiceSxsConfig interface","_cos_IServiceSxsConfig_SxsDirectory","comsvcs/IServiceSxsConfig::SxsDirectory","cos.iservicesxsconfig_sxsdirectory"]
old-location: cos\iservicesxsconfig_sxsdirectory.htm
tech.root: cos
ms.assetid: 5eb909a5-7730-4f0b-aee6-9bb8de076cea
ms.date: 12/05/2018
ms.keywords: IServiceSxsConfig interface [COM+],SxsDirectory method, IServiceSxsConfig.SxsDirectory, IServiceSxsConfig::SxsDirectory, SxsDirectory, SxsDirectory method [COM+], SxsDirectory method [COM+],IServiceSxsConfig interface, _cos_IServiceSxsConfig_SxsDirectory, comsvcs/IServiceSxsConfig::SxsDirectory, cos.iservicesxsconfig_sxsdirectory
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
 - IServiceSxsConfig::SxsDirectory
 - comsvcs/IServiceSxsConfig::SxsDirectory
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
 - IServiceSxsConfig.SxsDirectory
---

# IServiceSxsConfig::SxsDirectory


## -description

Sets the directory for the side-by-side assembly for the enclosed work.

## -parameters

### -param szSxsDirectory [in]

The name of the directory for the side-by-side assembly that is to be used for the enclosed work.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

This method must be called if a new side-by-side assembly domain is created using the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicesxsconfig-sxsconfig">SxsConfig</a>.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicesxsconfig">IServiceSxsConfig</a>