---
UID: NN:fsrmpipeline.IFsrmPipelineModuleImplementation
title: IFsrmPipelineModuleImplementation (fsrmpipeline.h)
description: Abstract interface for IFsrmClassifierModuleImplementation and IFsrmStorageModuleImplementation.
helpviewer_keywords: ["IFsrmPipelineModuleImplementation","IFsrmPipelineModuleImplementation interface [File Server Resource Manager]","IFsrmPipelineModuleImplementation interface [File Server Resource Manager]","described","fs.ifsrmpipelinemoduleimplementation","fsrm.ifsrmpipelinemoduleimplementation","fsrm/IFsrmPipelineModuleImplementation"]
old-location: fsrm\ifsrmpipelinemoduleimplementation.htm
tech.root: fsrm
ms.assetid: a4420b1e-e2e5-460c-948c-3c5f97d7a0e7
ms.date: 12/05/2018
ms.keywords: IFsrmPipelineModuleImplementation, IFsrmPipelineModuleImplementation interface [File Server Resource Manager], IFsrmPipelineModuleImplementation interface [File Server Resource Manager],described, fs.ifsrmpipelinemoduleimplementation, fsrm.ifsrmpipelinemoduleimplementation, fsrm/IFsrmPipelineModuleImplementation
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
 - IFsrmPipelineModuleImplementation
 - fsrmpipeline/IFsrmPipelineModuleImplementation
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
 - IFsrmPipelineModuleImplementation
---

# IFsrmPipelineModuleImplementation interface


## -description

Abstract interface for 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a> and 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>.

Classifiers and storage modules should not implement this interface. For more information, see 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a> or 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>.

## -inheritance

The <b>IFsrmPipelineModuleImplementation</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmPipelineModuleImplementation</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>
