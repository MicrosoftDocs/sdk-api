---
UID: NN:fsrmpipeline.IFsrmClassifierModuleImplementation
title: IFsrmClassifierModuleImplementation
author: windows-sdk-content
description: Classifier modules implement this interface. FSRM calls the module's implementation when it runs classification.
old-location: fsrm\ifsrmclassifiermoduleimplementation.htm
tech.root: fsrm
ms.assetid: f238c446-b268-4600-b6e3-ec772a5f7575
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: IFsrmClassifierModuleImplementation, IFsrmClassifierModuleImplementation interface [File Server Resource Manager], IFsrmClassifierModuleImplementation interface [File Server Resource Manager],described, fs.ifsrmclassifiermoduleimplementation, fsrm.ifsrmclassifiermoduleimplementation, fsrm/IFsrmClassifierModuleImplementation
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
 - IFsrmClassifierModuleImplementation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassifierModuleImplementation interface


## -description


Classifier modules implement this interface. FSRM calls the module's implementation when it runs 
    classification.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmClassifierModuleImplementation</b> interface inherits from <b>IFsrmPipelineModuleImplementation</b>. <b>IFsrmClassifierModuleImplementation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmClassifierModuleImplementation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab42430c-1e30-4576-b6f8-c0488b6230dd">DoesPropertyValueApply</a>
</td>
<td align="left" width="63%">
Queries the classifier to find out whether the specified property value applies to the file most recently 
       specified by the 
       <a href="https://msdn.microsoft.com/799f26c7-925e-4669-9571-128e10c51e9c">OnBeginFile</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70277473-de96-40e1-980b-4eec6e7b035d">GetPropertyValueToApply</a>
</td>
<td align="left" width="63%">
Retrieves the value from the classifier that should be applied for the specified property of the file most 
       recently specified by the 
       <a href="https://msdn.microsoft.com/799f26c7-925e-4669-9571-128e10c51e9c">OnBeginFile</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/799f26c7-925e-4669-9571-128e10c51e9c">OnBeginFile</a>
</td>
<td align="left" width="63%">
Instructs the classifier to prepare for processing a file with the specified property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52de3e11-89b3-4cf2-92f3-cc6dff686e0b">OnEndFile</a>
</td>
<td align="left" width="63%">
Instructs the classifier to perform any cleanup after processing a file.

</td>
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
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fbca8c4-7021-4183-b8f7-a32082da17fc">UseRulesAndDefinitions</a>
</td>
<td align="left" width="63%">
Specifies the collection of rules and relevant property definitions the classifier should expect to 
       process.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmClassifierModuleImplementation</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Dd878724(v=VS.85).aspx">LastModified</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The last time the classifier's internal rules were modified as a 64-bit 
      <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a4420b1e-e2e5-460c-948c-3c5f97d7a0e7">IFsrmPipelineModuleImplementation</a>



<a href="https://msdn.microsoft.com/8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6">IFsrmStorageModuleImplementation</a>
 

 

