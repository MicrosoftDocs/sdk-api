---
UID: NF:fsrmpipeline.IFsrmClassifierModuleDefinition.get_PropertiesAffected
title: IFsrmClassifierModuleDefinition::get_PropertiesAffected (fsrmpipeline.h)
description: The list of property names that the classifier can affect. (Get)
helpviewer_keywords: ["IFsrmClassifierModuleDefinition interface [File Server Resource Manager]","PropertiesAffected property","IFsrmClassifierModuleDefinition.PropertiesAffected","IFsrmClassifierModuleDefinition.get_PropertiesAffected","IFsrmClassifierModuleDefinition::PropertiesAffected","IFsrmClassifierModuleDefinition::get_PropertiesAffected","IFsrmClassifierModuleDefinition::put_PropertiesAffected","PropertiesAffected property [File Server Resource Manager]","PropertiesAffected property [File Server Resource Manager]","IFsrmClassifierModuleDefinition interface","fs.ifsrmclassifiermoduledefinition_propertiesaffected","fsrm.ifsrmclassifiermoduledefinition_propertiesaffected","fsrmpipeline/IFsrmClassifierModuleDefinition::PropertiesAffected","fsrmpipeline/IFsrmClassifierModuleDefinition::get_PropertiesAffected","fsrmpipeline/IFsrmClassifierModuleDefinition::put_PropertiesAffected","get_PropertiesAffected"]
old-location: fsrm\ifsrmclassifiermoduledefinition_propertiesaffected.htm
tech.root: fsrm
ms.assetid: 69f288d1-cc78-4af0-891b-c5c3ed8d2659
ms.date: 12/05/2018
ms.keywords: IFsrmClassifierModuleDefinition interface [File Server Resource Manager],PropertiesAffected property, IFsrmClassifierModuleDefinition.PropertiesAffected, IFsrmClassifierModuleDefinition.get_PropertiesAffected, IFsrmClassifierModuleDefinition::PropertiesAffected, IFsrmClassifierModuleDefinition::get_PropertiesAffected, IFsrmClassifierModuleDefinition::put_PropertiesAffected, PropertiesAffected property [File Server Resource Manager], PropertiesAffected property [File Server Resource Manager],IFsrmClassifierModuleDefinition interface, fs.ifsrmclassifiermoduledefinition_propertiesaffected, fsrm.ifsrmclassifiermoduledefinition_propertiesaffected, fsrmpipeline/IFsrmClassifierModuleDefinition::PropertiesAffected, fsrmpipeline/IFsrmClassifierModuleDefinition::get_PropertiesAffected, fsrmpipeline/IFsrmClassifierModuleDefinition::put_PropertiesAffected, get_PropertiesAffected
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
 - IFsrmClassifierModuleDefinition::get_PropertiesAffected
 - fsrmpipeline/IFsrmClassifierModuleDefinition::get_PropertiesAffected
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
 - IFsrmClassifierModuleDefinition.PropertiesAffected
 - IFsrmClassifierModuleDefinition.get_PropertiesAffected
 - IFsrmClassifierModuleDefinition.put_PropertiesAffected
---

# IFsrmClassifierModuleDefinition::get_PropertiesAffected


## -description

The list of property names that the classifier can affect.

This property is read/write.

## -parameters

## -remarks

This list is optional. Specify a list of properties only if you want to limit the properties that this classifier can affect; otherwise, if the list is empty, the classifier can affect any property in the file.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a>
