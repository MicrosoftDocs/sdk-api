---
UID: NF:fsrmpipeline.IFsrmPipelineModuleDefinition.put_SupportedExtensions
title: IFsrmPipelineModuleDefinition::put_SupportedExtensions
author: windows-sdk-content
description: The list of file extensions supported by this module.
old-location: fsrm\ifsrmpipelinemoduledefinition_supportedextensions.htm
old-project: Fsrm
ms.assetid: d83caabf-ea62-4d3d-83e3-7b95f4fcc103
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmPipelineModuleDefinition interface [File Server Resource Manager],SupportedExtensions property, IFsrmPipelineModuleDefinition.SupportedExtensions, IFsrmPipelineModuleDefinition.put_SupportedExtensions, IFsrmPipelineModuleDefinition::SupportedExtensions, IFsrmPipelineModuleDefinition::get_SupportedExtensions, IFsrmPipelineModuleDefinition::put_SupportedExtensions, SupportedExtensions property [File Server Resource Manager], SupportedExtensions property [File Server Resource Manager],IFsrmPipelineModuleDefinition interface, fs.ifsrmpipelinemoduledefinition_supportedextensions, fsrm.ifsrmpipelinemoduledefinition_supportedextensions, fsrmpipeline/IFsrmPipelineModuleDefinition::SupportedExtensions, fsrmpipeline/IFsrmPipelineModuleDefinition::get_SupportedExtensions, fsrmpipeline/IFsrmPipelineModuleDefinition::put_SupportedExtensions, put_SupportedExtensions
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmPipelineModuleDefinition::put_SupportedExtensions


## -description


The list of file extensions supported by this module.

This property is read/write.


## -parameters


## -remarks



This property is optional. Set this property only if you support a limited number of file types. FSRM uses the 
    list of extensions to determine the files that it sends to the module. If the list is empty, FSRM will send the 
    module all files.




## -see-also




<a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a>
 

 

