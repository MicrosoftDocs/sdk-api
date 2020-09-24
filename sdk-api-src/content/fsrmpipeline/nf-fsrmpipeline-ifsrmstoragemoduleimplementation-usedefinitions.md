---
UID: NF:fsrmpipeline.IFsrmStorageModuleImplementation.UseDefinitions
title: IFsrmStorageModuleImplementation::UseDefinitions (fsrmpipeline.h)
description: Specifies the property definitions FSRM recognizes.
helpviewer_keywords: ["IFsrmStorageModuleImplementation interface [File Server Resource Manager]","UseDefinitions method","IFsrmStorageModuleImplementation.UseDefinitions","IFsrmStorageModuleImplementation::UseDefinitions","UseDefinitions","UseDefinitions method [File Server Resource Manager]","UseDefinitions method [File Server Resource Manager]","IFsrmStorageModuleImplementation interface","fs.ifsrmstoragemoduleimplementation_usedefinitions","fsrm.ifsrmstoragemoduleimplementation_usedefinitions","fsrmpipeline/IFsrmStorageModuleImplementation::UseDefinitions"]
old-location: fsrm\ifsrmstoragemoduleimplementation_usedefinitions.htm
tech.root: fsrm
ms.assetid: d5683668-18c2-405b-aa56-8e7a9a1d5a9e
ms.date: 12/05/2018
ms.keywords: IFsrmStorageModuleImplementation interface [File Server Resource Manager],UseDefinitions method, IFsrmStorageModuleImplementation.UseDefinitions, IFsrmStorageModuleImplementation::UseDefinitions, UseDefinitions, UseDefinitions method [File Server Resource Manager], UseDefinitions method [File Server Resource Manager],IFsrmStorageModuleImplementation interface, fs.ifsrmstoragemoduleimplementation_usedefinitions, fsrm.ifsrmstoragemoduleimplementation_usedefinitions, fsrmpipeline/IFsrmStorageModuleImplementation::UseDefinitions
req.header: fsrmpipeline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmStorageModuleImplementation::UseDefinitions
 - fsrmpipeline/IFsrmStorageModuleImplementation::UseDefinitions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmStorageModuleImplementation.UseDefinitions
---

# IFsrmStorageModuleImplementation::UseDefinitions


## -description

Specifies the property definitions FSRM recognizes.

## -parameters

### -param propertyDefinitions [in]

Collection of property definitions that are currently defined by FSRM.

## -returns

The method returns the following return values.

Other values will result in the client application receiving a 
         <b>FSRM_E_MODULE_SESSION_INITIALIZATION</b> error.

<b>Windows Server 2008 R2:  </b>The client application will receive a <b>FSRM_E_UNEXPECTED</b> error.

## -remarks

The storage module may optionally use the collection of property definitions when determining how to load and 
    save particular properties as appropriate.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>