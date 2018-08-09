---
UID: NF:fsrmpipeline.IFsrmStorageModuleImplementation.LoadProperties
title: IFsrmStorageModuleImplementation::LoadProperties
author: windows-sdk-content
description: Instructs the storage module to load all properties.
old-location: fsrm\ifsrmstoragemoduleimplementation_loadproperties.htm
old-project: fsrm
ms.assetid: 05de6dfe-0f90-4866-bedc-72b8fea9dfac
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmStorageModuleImplementation interface [File Server Resource Manager],LoadProperties method, IFsrmStorageModuleImplementation.LoadProperties, IFsrmStorageModuleImplementation::LoadProperties, LoadProperties, LoadProperties method [File Server Resource Manager], LoadProperties method [File Server Resource Manager],IFsrmStorageModuleImplementation interface, fs.ifsrmstoragemoduleimplementation_loadproperties, fsrm.ifsrmstoragemoduleimplementation_loadproperties, fsrmpipeline/IFsrmStorageModuleImplementation::LoadProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmStorageModuleImplementation.LoadProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
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



The storage module must call the <a href="https://msdn.microsoft.com/d3322907-c832-49ef-bf21-2e4581251a88">IFsrmPropertyBag::SetFileProperty</a> method on the property bag that is passed in for each property it chooses to set.

If <b>FSRM_E_INCOMPATIBLE_FORMAT</b> or <b>FSRM_E_FILE_ENCRYPTED</b> is returned, FSRM will not indicate that the file has failed classification. If any other error value is returned, FSRM will indicate that the file has failed classification.




## -see-also




<a href="https://msdn.microsoft.com/8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6">IFsrmStorageModuleImplementation</a>
 

 

