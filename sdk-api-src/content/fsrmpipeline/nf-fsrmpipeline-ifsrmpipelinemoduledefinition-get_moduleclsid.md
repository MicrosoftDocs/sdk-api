---
UID: NF:fsrmpipeline.IFsrmPipelineModuleDefinition.get_ModuleClsid
title: IFsrmPipelineModuleDefinition::get_ModuleClsid (fsrmpipeline.h)
description: A string representation specifying the COM class identifier for the class that implements the module defined by this module definition. (Get)
helpviewer_keywords: ["IFsrmPipelineModuleDefinition interface [File Server Resource Manager]","ModuleClsid property","IFsrmPipelineModuleDefinition.ModuleClsid","IFsrmPipelineModuleDefinition.get_ModuleClsid","IFsrmPipelineModuleDefinition::ModuleClsid","IFsrmPipelineModuleDefinition::get_ModuleClsid","IFsrmPipelineModuleDefinition::put_ModuleClsid","ModuleClsid property [File Server Resource Manager]","ModuleClsid property [File Server Resource Manager]","IFsrmPipelineModuleDefinition interface","fs.ifsrmpipelinemoduledefinition_moduleclsid","fsrm.ifsrmpipelinemoduledefinition_moduleclsid","fsrmpipeline/IFsrmPipelineModuleDefinition::ModuleClsid","fsrmpipeline/IFsrmPipelineModuleDefinition::get_ModuleClsid","fsrmpipeline/IFsrmPipelineModuleDefinition::put_ModuleClsid","get_ModuleClsid"]
old-location: fsrm\ifsrmpipelinemoduledefinition_moduleclsid.htm
tech.root: fsrm
ms.assetid: a90c8836-cd7f-46d8-814c-6f798c930b4d
ms.date: 12/05/2018
ms.keywords: IFsrmPipelineModuleDefinition interface [File Server Resource Manager],ModuleClsid property, IFsrmPipelineModuleDefinition.ModuleClsid, IFsrmPipelineModuleDefinition.get_ModuleClsid, IFsrmPipelineModuleDefinition::ModuleClsid, IFsrmPipelineModuleDefinition::get_ModuleClsid, IFsrmPipelineModuleDefinition::put_ModuleClsid, ModuleClsid property [File Server Resource Manager], ModuleClsid property [File Server Resource Manager],IFsrmPipelineModuleDefinition interface, fs.ifsrmpipelinemoduledefinition_moduleclsid, fsrm.ifsrmpipelinemoduledefinition_moduleclsid, fsrmpipeline/IFsrmPipelineModuleDefinition::ModuleClsid, fsrmpipeline/IFsrmPipelineModuleDefinition::get_ModuleClsid, fsrmpipeline/IFsrmPipelineModuleDefinition::put_ModuleClsid, get_ModuleClsid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmPipelineModuleDefinition::get_ModuleClsid
 - fsrmpipeline/IFsrmPipelineModuleDefinition::get_ModuleClsid
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
 - IFsrmPipelineModuleDefinition.ModuleClsid
 - IFsrmPipelineModuleDefinition.get_ModuleClsid
 - IFsrmPipelineModuleDefinition.put_ModuleClsid
---

# IFsrmPipelineModuleDefinition::get_ModuleClsid


## -description

A string representation specifying the COM class identifier for the class that implements the module defined by this module definition.

This property is read/write.

## -parameters

## -remarks

Note that the COM class  identifier specified must refer to a class that implements <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleimplementation">IFsrmPipelineModuleImplementation</a>, which is inherited though <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a> or <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>, depending on the type of module.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a>
