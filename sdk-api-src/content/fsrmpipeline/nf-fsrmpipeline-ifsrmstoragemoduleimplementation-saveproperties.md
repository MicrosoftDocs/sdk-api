---
UID: NF:fsrmpipeline.IFsrmStorageModuleImplementation.SaveProperties
title: IFsrmStorageModuleImplementation::SaveProperties
author: windows-sdk-content
description: Instructs the storage module to save properties associated with a file.
old-location: fsrm\ifsrmstoragemoduleimplementation_saveproperties.htm
tech.root: fsrm
ms.assetid: 4d31db26-9d03-46f3-a902-401f9e0d9767
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: IFsrmStorageModuleImplementation interface [File Server Resource Manager],SaveProperties method, IFsrmStorageModuleImplementation.SaveProperties, IFsrmStorageModuleImplementation::SaveProperties, SaveProperties, SaveProperties method [File Server Resource Manager], SaveProperties method [File Server Resource Manager],IFsrmStorageModuleImplementation interface, fs.ifsrmstoragemoduleimplementation_saveproperties, fsrm.ifsrmstoragemoduleimplementation_saveproperties, fsrmpipeline/IFsrmStorageModuleImplementation::SaveProperties
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmStorageModuleImplementation.SaveProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmStorageModuleImplementation::SaveProperties


## -description


Instructs the storage module to save properties associated with a file.


## -parameters




### -param propertyBag [in]

Specifies the location to save properties.


## -returns



The method returns the following return values. Implementers should return an HRESULT error code for any other errors.




## -remarks



If <b>FSRM_E_INCOMPATIBLE_FORMAT</b> or <b>FSRM_E_FILE_ENCRYPTED</b> is returned, FSRM will not indicate that the file has failed classification. If any other error value is returned, FSRM will indicate that the file has failed classification.




## -see-also




<a href="https://msdn.microsoft.com/8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6">IFsrmStorageModuleImplementation</a>
 

 

