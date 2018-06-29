---
UID: NN:fsrmpipeline.IFsrmPipelineModuleImplementation
title: IFsrmPipelineModuleImplementation
author: windows-sdk-content
description: Abstract interface for IFsrmClassifierModuleImplementation and IFsrmStorageModuleImplementation.
old-location: fsrm\ifsrmpipelinemoduleimplementation.htm
old-project: Fsrm
ms.assetid: a4420b1e-e2e5-460c-948c-3c5f97d7a0e7
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IFsrmPipelineModuleImplementation, IFsrmPipelineModuleImplementation interface [File Server Resource Manager], IFsrmPipelineModuleImplementation interface [File Server Resource Manager],described, fs.ifsrmpipelinemoduleimplementation, fsrm.ifsrmpipelinemoduleimplementation, fsrm/IFsrmPipelineModuleImplementation
ms.prod: windows
ms.technology: windows-sdk
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
 - IFsrmPipelineModuleImplementation
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmPipelineModuleImplementation interface


## -description


Abstract interface for 
    <a href="https://msdn.microsoft.com/f238c446-b268-4600-b6e3-ec772a5f7575">IFsrmClassifierModuleImplementation</a> and 
    <a href="https://msdn.microsoft.com/8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6">IFsrmStorageModuleImplementation</a>.

Classifiers and storage modules should not implement this interface. For more information, see 
    <a href="https://msdn.microsoft.com/f238c446-b268-4600-b6e3-ec772a5f7575">IFsrmClassifierModuleImplementation</a> or 
    <a href="https://msdn.microsoft.com/8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6">IFsrmStorageModuleImplementation</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPipelineModuleImplementation</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFsrmPipelineModuleImplementation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/69d848b9-4143-4b6c-9a45-66ff44c54b66">OnLoad</a>
</td>
<td align="left" width="63%">
Initializes the pipeline module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0febde2-f067-4ca7-8c2b-2f09da9e7d23">OnUnload</a>
</td>
<td align="left" width="63%">
Notifies the module to perform any cleanup tasks.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f238c446-b268-4600-b6e3-ec772a5f7575">IFsrmClassifierModuleImplementation</a>



<a href="https://msdn.microsoft.com/8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6">IFsrmStorageModuleImplementation</a>
 

 

