---
UID: NF:fsrmpipeline.IFsrmStorageModuleImplementation.LoadProperties
title: IFsrmStorageModuleImplementation::LoadProperties (fsrmpipeline.h)
description: Instructs the storage module to load all properties.
helpviewer_keywords: ["IFsrmStorageModuleImplementation interface [File Server Resource Manager]","LoadProperties method","IFsrmStorageModuleImplementation.LoadProperties","IFsrmStorageModuleImplementation::LoadProperties","LoadProperties","LoadProperties method [File Server Resource Manager]","LoadProperties method [File Server Resource Manager]","IFsrmStorageModuleImplementation interface","fs.ifsrmstoragemoduleimplementation_loadproperties","fsrm.ifsrmstoragemoduleimplementation_loadproperties","fsrmpipeline/IFsrmStorageModuleImplementation::LoadProperties"]
old-location: fsrm\ifsrmstoragemoduleimplementation_loadproperties.htm
tech.root: fsrm
ms.assetid: 05de6dfe-0f90-4866-bedc-72b8fea9dfac
ms.date: 12/05/2018
ms.keywords: IFsrmStorageModuleImplementation interface [File Server Resource Manager],LoadProperties method, IFsrmStorageModuleImplementation.LoadProperties, IFsrmStorageModuleImplementation::LoadProperties, LoadProperties, LoadProperties method [File Server Resource Manager], LoadProperties method [File Server Resource Manager],IFsrmStorageModuleImplementation interface, fs.ifsrmstoragemoduleimplementation_loadproperties, fsrm.ifsrmstoragemoduleimplementation_loadproperties, fsrmpipeline/IFsrmStorageModuleImplementation::LoadProperties
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
 - IFsrmStorageModuleImplementation::LoadProperties
 - fsrmpipeline/IFsrmStorageModuleImplementation::LoadProperties
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
 - IFsrmStorageModuleImplementation.LoadProperties
---

# IFsrmStorageModuleImplementation::LoadProperties


## -description

Instructs the storage module to load all properties.

## -parameters

### -param propertyBag [in]

Specifies the properties to load.

## -returns

The method returns the following return values. Implementers should return an HRESULT error code for any other errors.

## -remarks

The storage module must call the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-setfileproperty">IFsrmPropertyBag::SetFileProperty</a> method on the property bag that is passed in for each property it chooses to set.

If <b>FSRM_E_INCOMPATIBLE_FORMAT</b> or <b>FSRM_E_FILE_ENCRYPTED</b> is returned, FSRM will not indicate that the file has failed classification. If any other error value is returned, FSRM will indicate that the file has failed classification.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>