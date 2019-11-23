---
UID: NN:fsrmpipeline.IFsrmClassifierModuleImplementation
title: IFsrmClassifierModuleImplementation (fsrmpipeline.h)

description: Classifier modules implement this interface. FSRM calls the module's implementation when it runs classification.
old-location: fsrm\ifsrmclassifiermoduleimplementation.htm
tech.root: fsrm
ms.assetid: f238c446-b268-4600-b6e3-ec772a5f7575

ms.date: 12/05/2018
ms.keywords: IFsrmClassifierModuleImplementation, IFsrmClassifierModuleImplementation interface [File Server Resource Manager], IFsrmClassifierModuleImplementation interface [File Server Resource Manager],described, fs.ifsrmclassifiermoduleimplementation, fsrm.ifsrmclassifiermoduleimplementation, fsrm/IFsrmClassifierModuleImplementation
ms.topic: interface
f1_keywords: 
 - "fsrmpipeline/IFsrmClassifierModuleImplementation"
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
 - IFsrmClassifierModuleImplementation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-doespropertyvalueapply">DoesPropertyValueApply</a>
</td>
<td align="left" width="63%">
Queries the classifier to find out whether the specified property value applies to the file most recently 
       specified by the 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-onbeginfile">OnBeginFile</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-getpropertyvaluetoapply">GetPropertyValueToApply</a>
</td>
<td align="left" width="63%">
Retrieves the value from the classifier that should be applied for the specified property of the file most 
       recently specified by the 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-onbeginfile">OnBeginFile</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-onbeginfile">OnBeginFile</a>
</td>
<td align="left" width="63%">
Instructs the classifier to prepare for processing a file with the specified property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-onendfile">OnEndFile</a>
</td>
<td align="left" width="63%">
Instructs the classifier to perform any cleanup after processing a file.

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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-userulesanddefinitions">UseRulesAndDefinitions</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/ifsrmclassifiermoduleimplementation-lastmodified">LastModified</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The last time the classifier's internal rules were modified as a 64-bit 
      <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleimplementation">IFsrmPipelineModuleImplementation</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>
 

 

