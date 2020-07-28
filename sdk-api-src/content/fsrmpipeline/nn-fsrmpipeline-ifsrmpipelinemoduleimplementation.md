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
f1_keywords:
- fsrmpipeline/IFsrmPipelineModuleImplementation
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- SrmSvc.dll
api_name:
- IFsrmPipelineModuleImplementation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmPipelineModuleImplementation interface


## -description


Abstract interface for 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a> and 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>.

Classifiers and storage modules should not implement this interface. For more information, see 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a> or 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPipelineModuleImplementation</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmPipelineModuleImplementation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmPipelineModuleImplementation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleimplementation-onload">OnLoad</a>
</td>
<td align="left" width="63%">
Initializes the pipeline module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleimplementation-onunload">OnUnload</a>
</td>
<td align="left" width="63%">
Notifies the module to perform any cleanup tasks.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>
 

 

