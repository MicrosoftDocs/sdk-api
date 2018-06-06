---
UID: NF:fsrmpipeline.IFsrmRule.get_ModuleDefinitionName
title: IFsrmRule::get_ModuleDefinitionName
author: windows-sdk-content
description: The name of the module definition that you want to run this rule.
old-location: fsrm\ifsrmrule_moduledefinitionname.htm
old-project: Fsrm
ms.assetid: b003b31b-fe40-446d-9db8-619dfcecc6c7
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmRule interface [File Server Resource Manager],ModuleDefinitionName property, IFsrmRule.ModuleDefinitionName, IFsrmRule.get_ModuleDefinitionName, IFsrmRule::ModuleDefinitionName, IFsrmRule::get_ModuleDefinitionName, IFsrmRule::put_ModuleDefinitionName, ModuleDefinitionName property [File Server Resource Manager], ModuleDefinitionName property [File Server Resource Manager],IFsrmRule interface, fs.ifsrmrule_moduledefinitionname, fsrm.ifsrmrule_moduledefinitionname, fsrmpipeline/IFsrmRule::ModuleDefinitionName, fsrmpipeline/IFsrmRule::get_ModuleDefinitionName, fsrmpipeline/IFsrmRule::put_ModuleDefinitionName, get_ModuleDefinitionName
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
 - IFsrmRule.ModuleDefinitionName
 - IFsrmRule.get_ModuleDefinitionName
 - IFsrmRule.put_ModuleDefinitionName
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmRule::get_ModuleDefinitionName


## -description


The name of the module definition that you want to run this rule.

This property is read/write.


## -parameters


## -remarks



FSRM provides a built-in classifier module named, Folder Classifier. The Folder Classifier classifies files based on their location (in which folder they are located). This classifier looks at the current path of the file and matches it with the path specified in the namespace roots of the classification rule. If the path is within the scope of the rule's namespace roots, then FSRM applies the rule to the file.

To get a list of modules that have been registered with FSRM, call the <a href="https://msdn.microsoft.com/eeda0802-e450-4a8b-a08c-135784540b17">IFsrmClassificationManager::EnumModuleDefinitions</a> method. To access a module's name, use the <a href="https://msdn.microsoft.com/486c659e-59af-4a82-bcb0-72d12c2d05df">IFsrmPipelineModuleDefinition.Name</a> property.




## -see-also




<a href="https://msdn.microsoft.com/e1de871f-a2c9-4787-a3e8-8c3428e9249e">IFsrmRule</a>
 

 

