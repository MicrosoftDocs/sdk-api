---
UID: NE:fsrmenums._FsrmPipelineModuleType
title: FsrmPipelineModuleType (fsrmenums.h)
description: Defines the types of modules that you can define.
helpviewer_keywords: ["FsrmPipelineModuleType","FsrmPipelineModuleType enumeration [File Server Resource Manager]","FsrmPipelineModuleType_Classifier","FsrmPipelineModuleType_Storage","FsrmPipelineModuleType_Unknown","fs.fsrmpipelinemoduletype","fsrm.fsrmpipelinemoduletype","fsrmenums/FsrmPipelineModuleType","fsrmenums/FsrmPipelineModuleType_Classifier","fsrmenums/FsrmPipelineModuleType_Storage","fsrmenums/FsrmPipelineModuleType_Unknown"]
old-location: fsrm\fsrmpipelinemoduletype.htm
tech.root: fsrm
ms.assetid: a482c371-a01c-486b-b25b-d22283dba652
ms.date: 12/05/2018
ms.keywords: FsrmPipelineModuleType, FsrmPipelineModuleType enumeration [File Server Resource Manager], FsrmPipelineModuleType_Classifier, FsrmPipelineModuleType_Storage, FsrmPipelineModuleType_Unknown, fs.fsrmpipelinemoduletype, fsrm.fsrmpipelinemoduletype, fsrmenums/FsrmPipelineModuleType, fsrmenums/FsrmPipelineModuleType_Classifier, fsrmenums/FsrmPipelineModuleType_Storage, fsrmenums/FsrmPipelineModuleType_Unknown
req.header: fsrmenums.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FsrmPipelineModuleType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmPipelineModuleType
 - fsrmenums/_FsrmPipelineModuleType
 - FsrmPipelineModuleType
 - fsrmenums/FsrmPipelineModuleType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmPipelineModuleType
---

# FsrmPipelineModuleType enumeration


## -description

Defines the types of modules that you can define.

## -enum-fields

### -field FsrmPipelineModuleType_Unknown:0

The module type is unknown; do not use this value.

### -field FsrmPipelineModuleType_Storage:1

The module is a storage module. A storage module persists property values for the files that it 
      supports.

### -field FsrmPipelineModuleType_Classifier:2

The module is a classifier module. A classifier module assigns property values to files based on 
      classification rules.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createmoduledefinition">IFsrmClassificationManager::CreateModuleDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enummoduledefinitions">IFsrmClassificationManager::EnumModuleDefinitions</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getmoduledefinition">IFsrmClassificationManager::GetModuleDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduledefinition-get_moduletype">IFsrmPipelineModuleDefinition.ModuleType</a>
