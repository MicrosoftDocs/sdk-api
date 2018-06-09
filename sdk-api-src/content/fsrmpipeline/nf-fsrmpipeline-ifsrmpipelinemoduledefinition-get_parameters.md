---
UID: NF:fsrmpipeline.IFsrmPipelineModuleDefinition.get_Parameters
title: IFsrmPipelineModuleDefinition::get_Parameters
author: windows-sdk-content
description: The optional parameters to pass to the module.
old-location: fsrm\ifsrmpipelinemoduledefinition_parameters.htm
old-project: Fsrm
ms.assetid: 71421c07-f7cd-4baf-80a1-47416d514f56
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IFsrmPipelineModuleDefinition interface [File Server Resource Manager],Parameters property, IFsrmPipelineModuleDefinition.Parameters, IFsrmPipelineModuleDefinition.get_Parameters, IFsrmPipelineModuleDefinition::Parameters, IFsrmPipelineModuleDefinition::get_Parameters, IFsrmPipelineModuleDefinition::put_Parameters, Parameters property [File Server Resource Manager], Parameters property [File Server Resource Manager],IFsrmPipelineModuleDefinition interface, fs.ifsrmpipelinemoduledefinition_parameters, fsrm.ifsrmpipelinemoduledefinition_parameters, fsrmpipeline/IFsrmPipelineModuleDefinition::Parameters, fsrmpipeline/IFsrmPipelineModuleDefinition::get_Parameters, fsrmpipeline/IFsrmPipelineModuleDefinition::put_Parameters, get_Parameters
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
 - IFsrmPipelineModuleDefinition.Parameters
 - IFsrmPipelineModuleDefinition.get_Parameters
 - IFsrmPipelineModuleDefinition.put_Parameters
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmPipelineModuleDefinition::get_Parameters


## -description


The optional parameters to pass to the module.

This property is read/write.


## -parameters


## -remarks



There is no limit to length of the parameter name or value, nor is there a limit the number of parameters that you can specify. Specifying a parameter without a value is valid (for example, "parameter=").

The parameters are included in the module definition that FSRM passes to the module's <a href="https://msdn.microsoft.com/69d848b9-4143-4b6c-9a45-66ff44c54b66">IFsrmPipelineModuleImplementation::OnLoad</a> implementation.




## -see-also




<a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a>
 

 

