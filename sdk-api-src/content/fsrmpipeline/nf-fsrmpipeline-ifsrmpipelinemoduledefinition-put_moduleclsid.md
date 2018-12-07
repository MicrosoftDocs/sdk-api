---
UID: NF:fsrmpipeline.IFsrmPipelineModuleDefinition.put_ModuleClsid
title: IFsrmPipelineModuleDefinition::put_ModuleClsid
author: windows-sdk-content
description: A string representation specifying the COM class identifier for the class that implements the module defined by this module definition.
old-location: fsrm\ifsrmpipelinemoduledefinition_moduleclsid.htm
tech.root: fsrm
ms.assetid: a90c8836-cd7f-46d8-814c-6f798c930b4d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmPipelineModuleDefinition interface [File Server Resource Manager],ModuleClsid property, IFsrmPipelineModuleDefinition.ModuleClsid, IFsrmPipelineModuleDefinition.put_ModuleClsid, IFsrmPipelineModuleDefinition::ModuleClsid, IFsrmPipelineModuleDefinition::get_ModuleClsid, IFsrmPipelineModuleDefinition::put_ModuleClsid, ModuleClsid property [File Server Resource Manager], ModuleClsid property [File Server Resource Manager],IFsrmPipelineModuleDefinition interface, fs.ifsrmpipelinemoduledefinition_moduleclsid, fsrm.ifsrmpipelinemoduledefinition_moduleclsid, fsrmpipeline/IFsrmPipelineModuleDefinition::ModuleClsid, fsrmpipeline/IFsrmPipelineModuleDefinition::get_ModuleClsid, fsrmpipeline/IFsrmPipelineModuleDefinition::put_ModuleClsid, put_ModuleClsid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmPipelineModuleDefinition::put_ModuleClsid


## -description


A string representation specifying the COM class identifier for the class that implements the module defined by this module definition.

This property is read/write.


## -parameters


## -remarks



Note that the COM class  identifier specified must refer to a class that implements <a href="https://msdn.microsoft.com/a4420b1e-e2e5-460c-948c-3c5f97d7a0e7">IFsrmPipelineModuleImplementation</a>, which is inherited though <a href="https://msdn.microsoft.com/f238c446-b268-4600-b6e3-ec772a5f7575">IFsrmClassifierModuleImplementation</a> or <a href="https://msdn.microsoft.com/8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6">IFsrmStorageModuleImplementation</a>, depending on the type of module.




## -see-also




<a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a>
 

 

