---
UID: NF:fsrmpipeline.IFsrmRule.get_ModuleDefinitionName
title: IFsrmRule::get_ModuleDefinitionName (fsrmpipeline.h)
description: The name of the module definition that you want to run this rule.helpviewer_keywords: ["IFsrmRule interface [File Server Resource Manager]","ModuleDefinitionName property","IFsrmRule.ModuleDefinitionName","IFsrmRule.get_ModuleDefinitionName","IFsrmRule::ModuleDefinitionName","IFsrmRule::get_ModuleDefinitionName","IFsrmRule::put_ModuleDefinitionName","ModuleDefinitionName property [File Server Resource Manager]","ModuleDefinitionName property [File Server Resource Manager]","IFsrmRule interface","fs.ifsrmrule_moduledefinitionname","fsrm.ifsrmrule_moduledefinitionname","fsrmpipeline/IFsrmRule::ModuleDefinitionName","fsrmpipeline/IFsrmRule::get_ModuleDefinitionName","fsrmpipeline/IFsrmRule::put_ModuleDefinitionName","get_ModuleDefinitionName"]
old-location: fsrm\ifsrmrule_moduledefinitionname.htm
tech.root: fsrm
ms.assetid: b003b31b-fe40-446d-9db8-619dfcecc6c7
ms.date: 12/05/2018
ms.keywords: IFsrmRule interface [File Server Resource Manager],ModuleDefinitionName property, IFsrmRule.ModuleDefinitionName, IFsrmRule.get_ModuleDefinitionName, IFsrmRule::ModuleDefinitionName, IFsrmRule::get_ModuleDefinitionName, IFsrmRule::put_ModuleDefinitionName, ModuleDefinitionName property [File Server Resource Manager], ModuleDefinitionName property [File Server Resource Manager],IFsrmRule interface, fs.ifsrmrule_moduledefinitionname, fsrm.ifsrmrule_moduledefinitionname, fsrmpipeline/IFsrmRule::ModuleDefinitionName, fsrmpipeline/IFsrmRule::get_ModuleDefinitionName, fsrmpipeline/IFsrmRule::put_ModuleDefinitionName, get_ModuleDefinitionName
f1_keywords:
- fsrmpipeline/IFsrmRule.ModuleDefinitionName
dev_langs:
- c++
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
- IFsrmRule.ModuleDefinitionName
- IFsrmRule.get_ModuleDefinitionName
- IFsrmRule.put_ModuleDefinitionName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmRule::get_ModuleDefinitionName


## -description


The name of the module definition that you want to run this rule.

This property is read/write.


## -parameters


## -remarks



FSRM provides a built-in classifier module named, Folder Classifier. The Folder Classifier classifies files based on their location (in which folder they are located). This classifier looks at the current path of the file and matches it with the path specified in the namespace roots of the classification rule. If the path is within the scope of the rule's namespace roots, then FSRM applies the rule to the file.

To get a list of modules that have been registered with FSRM, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enummoduledefinitions">IFsrmClassificationManager::EnumModuleDefinitions</a> method. To access a module's name, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduledefinition-get_name">IFsrmPipelineModuleDefinition.Name</a> property.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmrule">IFsrmRule</a>
 

 

