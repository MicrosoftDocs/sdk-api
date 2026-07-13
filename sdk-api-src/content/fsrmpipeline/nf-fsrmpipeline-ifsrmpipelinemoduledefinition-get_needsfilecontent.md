---
UID: NF:fsrmpipeline.IFsrmPipelineModuleDefinition.get_NeedsFileContent
title: IFsrmPipelineModuleDefinition::get_NeedsFileContent (fsrmpipeline.h)
description: Determines whether the module needs to read the contents of the file. (Get)
helpviewer_keywords: ["IFsrmPipelineModuleDefinition interface [File Server Resource Manager]","NeedsFileContent property","IFsrmPipelineModuleDefinition.NeedsFileContent","IFsrmPipelineModuleDefinition.get_NeedsFileContent","IFsrmPipelineModuleDefinition::NeedsFileContent","IFsrmPipelineModuleDefinition::get_NeedsFileContent","IFsrmPipelineModuleDefinition::put_NeedsFileContent","NeedsFileContent property [File Server Resource Manager]","NeedsFileContent property [File Server Resource Manager]","IFsrmPipelineModuleDefinition interface","fs.ifsrmpipelinemoduledefinition_needsfilecontent","fsrm.ifsrmpipelinemoduledefinition_needsfilecontent","fsrmpipeline/IFsrmPipelineModuleDefinition::NeedsFileContent","fsrmpipeline/IFsrmPipelineModuleDefinition::get_NeedsFileContent","fsrmpipeline/IFsrmPipelineModuleDefinition::put_NeedsFileContent","get_NeedsFileContent"]
old-location: fsrm\ifsrmpipelinemoduledefinition_needsfilecontent.htm
tech.root: fsrm
ms.assetid: c2cbcfe1-113c-4eb9-9dea-5619bcda58a2
ms.date: 12/05/2018
ms.keywords: IFsrmPipelineModuleDefinition interface [File Server Resource Manager],NeedsFileContent property, IFsrmPipelineModuleDefinition.NeedsFileContent, IFsrmPipelineModuleDefinition.get_NeedsFileContent, IFsrmPipelineModuleDefinition::NeedsFileContent, IFsrmPipelineModuleDefinition::get_NeedsFileContent, IFsrmPipelineModuleDefinition::put_NeedsFileContent, NeedsFileContent property [File Server Resource Manager], NeedsFileContent property [File Server Resource Manager],IFsrmPipelineModuleDefinition interface, fs.ifsrmpipelinemoduledefinition_needsfilecontent, fsrm.ifsrmpipelinemoduledefinition_needsfilecontent, fsrmpipeline/IFsrmPipelineModuleDefinition::NeedsFileContent, fsrmpipeline/IFsrmPipelineModuleDefinition::get_NeedsFileContent, fsrmpipeline/IFsrmPipelineModuleDefinition::put_NeedsFileContent, get_NeedsFileContent
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
 - IFsrmPipelineModuleDefinition::get_NeedsFileContent
 - fsrmpipeline/IFsrmPipelineModuleDefinition::get_NeedsFileContent
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
 - IFsrmPipelineModuleDefinition.NeedsFileContent
 - IFsrmPipelineModuleDefinition.get_NeedsFileContent
 - IFsrmPipelineModuleDefinition.put_NeedsFileContent
---

# IFsrmPipelineModuleDefinition::get_NeedsFileContent


## -description

Determines whether the module needs to read the contents of the file.

This property is read/write.

## -parameters

## -remarks

If the 
    <b>NeedsFileContent</b> property 
    value is <b>VARIANT_TRUE</b>, FSRM will provide a stream for a file's contents to the module. 
    This may be necessary if a classification module needs to analyze the contents of the file to determine the 
    property values or if a storage module handles property values embedded in the file's contents

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a>
