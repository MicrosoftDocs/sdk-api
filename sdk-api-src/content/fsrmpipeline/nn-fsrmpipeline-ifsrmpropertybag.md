---
UID: NN:fsrmpipeline.IFsrmPropertyBag
title: IFsrmPropertyBag (fsrmpipeline.h)
description: Contains the classification properties for a file.
helpviewer_keywords: ["IFsrmPropertyBag","IFsrmPropertyBag interface [File Server Resource Manager]","IFsrmPropertyBag interface [File Server Resource Manager]","described","fs.ifsrmpropertybag","fsrm.ifsrmpropertybag","fsrm/IFsrmPropertyBag"]
old-location: fsrm\ifsrmpropertybag.htm
tech.root: fsrm
ms.assetid: 237f024d-2b1d-45d5-a63d-c530426278e6
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyBag, IFsrmPropertyBag interface [File Server Resource Manager], IFsrmPropertyBag interface [File Server Resource Manager],described, fs.ifsrmpropertybag, fsrm.ifsrmpropertybag, fsrm/IFsrmPropertyBag
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmPropertyBag
 - fsrmpipeline/IFsrmPropertyBag
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
 - IFsrmPropertyBag
---

# IFsrmPropertyBag interface


## -description

Contains the classification properties for a file.

FSRM passes this interface to your 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleimplementation">IFsrmPipelineModuleImplementation</a> 
    implementation. For more information, see the Remarks section.

## -inheritance

The <b>IFsrmPropertyBag</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmPropertyBag</b> also has these types of members:

## -remarks

A property bag contains an in-memory copy of all the properties for a file. The list of properties in the 
    property bag may include additional properties not defined in FSRM. These properties can be the result of other 
    metadata in the file.

This interface can be sent to 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-doespropertyvalueapply">IFsrmClassifierModuleImplementation::DoesPropertyValueApply</a> 
    and 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-getpropertyvaluetoapply">IFsrmClassifierModuleImplementation::GetPropertyValueToApply</a> 
    if a classifier module is implemented, or to 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduleimplementation-loadproperties">IFsrmStorageModuleImplementation::LoadProperties</a> 
    and 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduleimplementation-saveproperties">IFsrmStorageModuleImplementation::SaveProperties</a> 
    if a storage module is implemented.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleimplementation">IFsrmPipelineModuleImplementation</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>
