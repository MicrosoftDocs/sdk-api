---
UID: NN:fsrmpipeline.IFsrmPipelineModuleDefinition
title: IFsrmPipelineModuleDefinition (fsrmpipeline.h)
description: Defines a module that is used to classify files or store and retrieve properties from files.
helpviewer_keywords: ["IFsrmPipelineModuleDefinition","IFsrmPipelineModuleDefinition interface [File Server Resource Manager]","IFsrmPipelineModuleDefinition interface [File Server Resource Manager]","described","fs.ifsrmpipelinemoduledefinition","fsrm.ifsrmpipelinemoduledefinition","fsrm/IFsrmPipelineModuleDefinition"]
old-location: fsrm\ifsrmpipelinemoduledefinition.htm
tech.root: fsrm
ms.assetid: 982c82a4-466d-476e-ad17-8f6f1c309c79
ms.date: 12/05/2018
ms.keywords: IFsrmPipelineModuleDefinition, IFsrmPipelineModuleDefinition interface [File Server Resource Manager], IFsrmPipelineModuleDefinition interface [File Server Resource Manager],described, fs.ifsrmpipelinemoduledefinition, fsrm.ifsrmpipelinemoduledefinition, fsrm/IFsrmPipelineModuleDefinition
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
 - IFsrmPipelineModuleDefinition
 - fsrmpipeline/IFsrmPipelineModuleDefinition
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
 - IFsrmPipelineModuleDefinition
---

# IFsrmPipelineModuleDefinition interface


## -description

Defines a module that is used to classify files or store and retrieve properties from 
    files.

To create a module definition, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createmoduledefinition">IFsrmClassificationManager::CreateModuleDefinition</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enummoduledefinitions">IFsrmClassificationManager::EnumModuleDefinitions</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getmoduledefinition">IFsrmClassificationManager::GetModuleDefinition</a>
</li>
</ul>This is the base class for module definition interfaces. Query this interface to get the interface for the 
    module type specified in the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduledefinition-get_moduletype">ModuleType</a> property. For 
    example, if <b>ModuleType</b> is 
    <b>FsrmPipelineModuleType_Classifier</b>, query this interface for the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a> 
    interface.

## -remarks

The name and module type identify a unique module (a classifier module and storage module can use the same 
    name).

When de-registering a module programmatically (calling 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-delete">Delete</a> followed by 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">Commit</a>), the developer should ensure that there are no 
    active classification rules that use that module. If this is not properly performed, the rules will produce errors 
    during classification runs and the UI will reflect a module that is no longer available.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduledefinition">IFsrmStorageModuleDefinition</a>