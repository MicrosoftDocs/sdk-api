---
UID: NF:fsrmpipeline.IFsrmPipelineModuleDefinition.get_SupportedExtensions
title: IFsrmPipelineModuleDefinition::get_SupportedExtensions (fsrmpipeline.h)
description: The list of file extensions supported by this module. (Get)
helpviewer_keywords: ["IFsrmPipelineModuleDefinition interface [File Server Resource Manager]","SupportedExtensions property","IFsrmPipelineModuleDefinition.SupportedExtensions","IFsrmPipelineModuleDefinition.get_SupportedExtensions","IFsrmPipelineModuleDefinition::SupportedExtensions","IFsrmPipelineModuleDefinition::get_SupportedExtensions","IFsrmPipelineModuleDefinition::put_SupportedExtensions","SupportedExtensions property [File Server Resource Manager]","SupportedExtensions property [File Server Resource Manager]","IFsrmPipelineModuleDefinition interface","fs.ifsrmpipelinemoduledefinition_supportedextensions","fsrm.ifsrmpipelinemoduledefinition_supportedextensions","fsrmpipeline/IFsrmPipelineModuleDefinition::SupportedExtensions","fsrmpipeline/IFsrmPipelineModuleDefinition::get_SupportedExtensions","fsrmpipeline/IFsrmPipelineModuleDefinition::put_SupportedExtensions","get_SupportedExtensions"]
old-location: fsrm\ifsrmpipelinemoduledefinition_supportedextensions.htm
tech.root: fsrm
ms.assetid: d83caabf-ea62-4d3d-83e3-7b95f4fcc103
ms.date: 12/05/2018
ms.keywords: IFsrmPipelineModuleDefinition interface [File Server Resource Manager],SupportedExtensions property, IFsrmPipelineModuleDefinition.SupportedExtensions, IFsrmPipelineModuleDefinition.get_SupportedExtensions, IFsrmPipelineModuleDefinition::SupportedExtensions, IFsrmPipelineModuleDefinition::get_SupportedExtensions, IFsrmPipelineModuleDefinition::put_SupportedExtensions, SupportedExtensions property [File Server Resource Manager], SupportedExtensions property [File Server Resource Manager],IFsrmPipelineModuleDefinition interface, fs.ifsrmpipelinemoduledefinition_supportedextensions, fsrm.ifsrmpipelinemoduledefinition_supportedextensions, fsrmpipeline/IFsrmPipelineModuleDefinition::SupportedExtensions, fsrmpipeline/IFsrmPipelineModuleDefinition::get_SupportedExtensions, fsrmpipeline/IFsrmPipelineModuleDefinition::put_SupportedExtensions, get_SupportedExtensions
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
 - IFsrmPipelineModuleDefinition::get_SupportedExtensions
 - fsrmpipeline/IFsrmPipelineModuleDefinition::get_SupportedExtensions
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
 - IFsrmPipelineModuleDefinition.SupportedExtensions
 - IFsrmPipelineModuleDefinition.get_SupportedExtensions
 - IFsrmPipelineModuleDefinition.put_SupportedExtensions
---

# IFsrmPipelineModuleDefinition::get_SupportedExtensions


## -description

The list of file extensions supported by this module.

This property is read/write.

## -parameters

## -remarks

This property is optional. Set this property only if you support a limited number of file types. FSRM uses the 
    list of extensions to determine the files that it sends to the module. If the list is empty, FSRM will send the 
    module all files.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a>
