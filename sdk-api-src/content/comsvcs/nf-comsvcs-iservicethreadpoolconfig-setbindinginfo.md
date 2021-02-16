---
UID: NF:comsvcs.IServiceThreadPoolConfig.SetBindingInfo
title: IServiceThreadPoolConfig::SetBindingInfo (comsvcs.h)
description: Binds all work submitted by the activity to a single single-threaded apartment.
helpviewer_keywords: ["IServiceThreadPoolConfig interface [COM+]","SetBindingInfo method","IServiceThreadPoolConfig.SetBindingInfo","IServiceThreadPoolConfig::SetBindingInfo","SetBindingInfo","SetBindingInfo method [COM+]","SetBindingInfo method [COM+]","IServiceThreadPoolConfig interface","_cos_IServiceThreadPoolConfig_SetBindingInfo","comsvcs/IServiceThreadPoolConfig::SetBindingInfo","cos.iservicethreadpoolconfig_setbindinginfo"]
old-location: cos\iservicethreadpoolconfig_setbindinginfo.htm
tech.root: cos
ms.assetid: 9d2c4e6f-aa12-4874-a8e0-ca21a981b43f
ms.date: 12/05/2018
ms.keywords: IServiceThreadPoolConfig interface [COM+],SetBindingInfo method, IServiceThreadPoolConfig.SetBindingInfo, IServiceThreadPoolConfig::SetBindingInfo, SetBindingInfo, SetBindingInfo method [COM+], SetBindingInfo method [COM+],IServiceThreadPoolConfig interface, _cos_IServiceThreadPoolConfig_SetBindingInfo, comsvcs/IServiceThreadPoolConfig::SetBindingInfo, cos.iservicethreadpoolconfig_setbindinginfo
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
 - IServiceThreadPoolConfig::SetBindingInfo
 - comsvcs/IServiceThreadPoolConfig::SetBindingInfo
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
 - IServiceThreadPoolConfig.SetBindingInfo
---

# IServiceThreadPoolConfig::SetBindingInfo


## -description

Binds all work submitted by the activity to a single single-threaded apartment.

## -parameters

### -param binding [in]

A value from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_binding">CSC_Binding</a> enumeration.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicethreadpoolconfig">IServiceThreadPoolConfig</a>