---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

