---
UID: NF:comsvcs.IAssemblyLocator.GetModules
title: IAssemblyLocator::GetModules (comsvcs.h)
description: Used to get the names of the modules that are contained in an assembly.
helpviewer_keywords: ["GetModules","GetModules method [COM+]","GetModules method [COM+]","IAssemblyLocator interface","IAssemblyLocator interface [COM+]","GetModules method","IAssemblyLocator.GetModules","IAssemblyLocator::GetModules","_cos_IAssemblyLocator_GetModules","comsvcs/IAssemblyLocator::GetModules","cos.iassemblylocator_getmodules"]
old-location: cos\iassemblylocator_getmodules.htm
tech.root: cos
ms.assetid: 5483c500-ac11-4f1d-b89c-37b6a718a735
ms.date: 12/05/2018
ms.keywords: GetModules, GetModules method [COM+], GetModules method [COM+],IAssemblyLocator interface, IAssemblyLocator interface [COM+],GetModules method, IAssemblyLocator.GetModules, IAssemblyLocator::GetModules, _cos_IAssemblyLocator_GetModules, comsvcs/IAssemblyLocator::GetModules, cos.iassemblylocator_getmodules
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
 - IAssemblyLocator::GetModules
 - comsvcs/IAssemblyLocator::GetModules
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
 - IAssemblyLocator.GetModules
---

# IAssemblyLocator::GetModules


## -description

Used to get the names of the modules that are contained in an assembly.

## -parameters

### -param applicationDir [in]

The directory containing the application.

### -param applicationName [in]

The name of the application domain.

### -param assemblyName [in]

The name of the assembly.

### -param pModules [out]

An array listing the names of the modules in the assembly.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iassemblylocator">IAssemblyLocator</a>