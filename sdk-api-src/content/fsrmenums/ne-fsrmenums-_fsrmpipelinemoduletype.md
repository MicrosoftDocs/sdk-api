---
UID: NE:fsrmenums._FsrmPipelineModuleType
title: "_FsrmPipelineModuleType"
author: windows-sdk-content
description: Defines the types of modules that you can define.
old-location: fsrm\fsrmpipelinemoduletype.htm
old-project: fsrm
ms.assetid: a482c371-a01c-486b-b25b-d22283dba652
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: FsrmPipelineModuleType, FsrmPipelineModuleType enumeration [File Server Resource Manager], FsrmPipelineModuleType_Classifier, FsrmPipelineModuleType_Storage, FsrmPipelineModuleType_Unknown, _FsrmPipelineModuleType, fs.fsrmpipelinemoduletype, fsrm.fsrmpipelinemoduletype, fsrmenums/FsrmPipelineModuleType, fsrmenums/FsrmPipelineModuleType_Classifier, fsrmenums/FsrmPipelineModuleType_Storage, fsrmenums/FsrmPipelineModuleType_Unknown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FsrmPipelineModuleType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmPipelineModuleType
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmPipelineModuleType enumeration


## -description


Defines the types of modules that you can define.


## -enum-fields




### -field FsrmPipelineModuleType_Unknown

The module type is unknown; do not use this value.


### -field FsrmPipelineModuleType_Storage

The module is a storage module. A storage module persists property values for the files that it 
      supports.


### -field FsrmPipelineModuleType_Classifier

The module is a classifier module. A classifier module assigns property values to files based on 
      classification rules.


## -see-also




<a href="https://msdn.microsoft.com/1964f4b6-b4e0-45a2-aca1-2e3dc44745a4">IFsrmClassificationManager::CreateModuleDefinition</a>



<a href="https://msdn.microsoft.com/eeda0802-e450-4a8b-a08c-135784540b17">IFsrmClassificationManager::EnumModuleDefinitions</a>



<a href="https://msdn.microsoft.com/41272218-25af-4c8f-8730-37a08a7fad4f">IFsrmClassificationManager::GetModuleDefinition</a>



<a href="https://msdn.microsoft.com/8cf3069d-8ad1-455b-baea-29c30cef1672">IFsrmPipelineModuleDefinition.ModuleType</a>
 

 

