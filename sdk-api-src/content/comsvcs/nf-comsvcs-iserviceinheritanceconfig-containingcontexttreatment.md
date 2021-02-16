---
UID: NF:comsvcs.IServiceInheritanceConfig.ContainingContextTreatment
title: IServiceInheritanceConfig::ContainingContextTreatment (comsvcs.h)
description: Determines whether the containing context is based on the current context.
helpviewer_keywords: ["ContainingContextTreatment","ContainingContextTreatment method [COM+]","ContainingContextTreatment method [COM+]","IServiceInheritanceConfig interface","IServiceInheritanceConfig interface [COM+]","ContainingContextTreatment method","IServiceInheritanceConfig.ContainingContextTreatment","IServiceInheritanceConfig::ContainingContextTreatment","_cos_IServiceInheritanceConfig_ContainingContextTreatment","comsvcs/IServiceInheritanceConfig::ContainingContextTreatment","cos.iserviceinheritanceconfig_containingcontexttreatment"]
old-location: cos\iserviceinheritanceconfig_containingcontexttreatment.htm
tech.root: cos
ms.assetid: 05009c50-1d39-46f7-b549-281342d07f5b
ms.date: 12/05/2018
ms.keywords: ContainingContextTreatment, ContainingContextTreatment method [COM+], ContainingContextTreatment method [COM+],IServiceInheritanceConfig interface, IServiceInheritanceConfig interface [COM+],ContainingContextTreatment method, IServiceInheritanceConfig.ContainingContextTreatment, IServiceInheritanceConfig::ContainingContextTreatment, _cos_IServiceInheritanceConfig_ContainingContextTreatment, comsvcs/IServiceInheritanceConfig::ContainingContextTreatment, cos.iserviceinheritanceconfig_containingcontexttreatment
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
 - IServiceInheritanceConfig::ContainingContextTreatment
 - comsvcs/IServiceInheritanceConfig::ContainingContextTreatment
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
 - IServiceInheritanceConfig.ContainingContextTreatment
---

# IServiceInheritanceConfig::ContainingContextTreatment


## -description

Determines whether the containing context is based on the current context.

## -parameters

### -param inheritanceConfig [in]

A value from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> enumeration.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceinheritanceconfig">IServiceInheritanceConfig</a>