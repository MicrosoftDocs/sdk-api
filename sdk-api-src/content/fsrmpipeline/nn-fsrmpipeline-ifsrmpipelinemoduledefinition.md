---
UID: NN:fsrmpipeline.IFsrmPipelineModuleDefinition
title: IFsrmPipelineModuleDefinition
author: windows-sdk-content
description: Defines a module that is used to classify files or store and retrieve properties from files.
old-location: fsrm\ifsrmpipelinemoduledefinition.htm
tech.root: fsrm
ms.assetid: 982c82a4-466d-476e-ad17-8f6f1c309c79
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmPipelineModuleDefinition, IFsrmPipelineModuleDefinition interface [File Server Resource Manager], IFsrmPipelineModuleDefinition interface [File Server Resource Manager],described, fs.ifsrmpipelinemoduledefinition, fsrm.ifsrmpipelinemoduledefinition, fsrm/IFsrmPipelineModuleDefinition
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFsrmPipelineModuleDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmPipelineModuleDefinition interface


## -description


Defines a module that is used to classify files or store and retrieve properties from 
    files.

To create a module definition, call the 
    <a href="https://msdn.microsoft.com/1964f4b6-b4e0-45a2-aca1-2e3dc44745a4">IFsrmClassificationManager::CreateModuleDefinition</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/eeda0802-e450-4a8b-a08c-135784540b17">IFsrmClassificationManager::EnumModuleDefinitions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/41272218-25af-4c8f-8730-37a08a7fad4f">IFsrmClassificationManager::GetModuleDefinition</a>
</li>
</ul>This is the base class for module definition interfaces. Query this interface to get the interface for the 
    module type specified in the 
    <a href="https://msdn.microsoft.com/8cf3069d-8ad1-455b-baea-29c30cef1672">ModuleType</a> property. For 
    example, if <b>ModuleType</b> is 
    <b>FsrmPipelineModuleType_Classifier</b>, query this interface for the 
    <a href="https://msdn.microsoft.com/6e691670-d7d7-48cb-8a81-ee8828b39b30">IFsrmClassifierModuleDefinition</a> 
    interface.


## -remarks



The name and module type identify a unique module (a classifier module and storage module can use the same 
    name).

When de-registering a module programmatically (calling 
    <a href="https://msdn.microsoft.com/ce8a17fe-377b-4a0e-9a95-7dc25a1411ce">Delete</a> followed by 
    <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">Commit</a>), the developer should ensure that there are no 
    active classification rules that use that module. If this is not properly performed, the rules will produce errors 
    during classification runs and the UI will reflect a module that is no longer available.




## -see-also




<a href="https://msdn.microsoft.com/6e691670-d7d7-48cb-8a81-ee8828b39b30">IFsrmClassifierModuleDefinition</a>



<a href="https://msdn.microsoft.com/bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7">IFsrmObject</a>



<a href="https://msdn.microsoft.com/68ecb5e6-61b0-488f-b6bb-181f253de70e">IFsrmStorageModuleDefinition</a>
 

 

