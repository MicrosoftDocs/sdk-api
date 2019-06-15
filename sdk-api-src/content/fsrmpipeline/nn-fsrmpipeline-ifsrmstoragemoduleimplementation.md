---
UID: NN:fsrmpipeline.IFsrmStorageModuleImplementation
title: IFsrmStorageModuleImplementation (fsrmpipeline.h)
author: windows-sdk-content
description: Storage modules implement this interface.
old-location: fsrm\ifsrmstoragemoduleimplementation.htm
tech.root: fsrm
ms.assetid: 8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmStorageModuleImplementation, IFsrmStorageModuleImplementation interface [File Server Resource Manager], IFsrmStorageModuleImplementation interface [File Server Resource Manager],described, fs.ifsrmstoragemoduleimplementation, fsrm.ifsrmstoragemoduleimplementation, fsrm/IFsrmStorageModuleImplementation
ms.topic: interface
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
 - IFsrmStorageModuleImplementation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmStorageModuleImplementation interface


## -description


Storage modules implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmStorageModuleImplementation</b> interface inherits from <b>IFsrmPipelineModuleImplementation</b>. <b>IFsrmStorageModuleImplementation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmStorageModuleImplementation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduleimplementation-loadproperties">LoadProperties</a>
</td>
<td align="left" width="63%">
Instructs the storage module to load properties associated with a file.

</td>
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
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduleimplementation-saveproperties">SaveProperties</a>
</td>
<td align="left" width="63%">
Instructs the storage module to save properties associated with a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduleimplementation-usedefinitions">UseDefinitions</a>
</td>
<td align="left" width="63%">
Specifies the property definitions FSRM recognizes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleimplementation">IFsrmPipelineModuleImplementation</a>
 

 

