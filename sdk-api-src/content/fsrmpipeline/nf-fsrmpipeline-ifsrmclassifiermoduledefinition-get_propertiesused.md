---
UID: NF:fsrmpipeline.IFsrmClassifierModuleDefinition.get_PropertiesUsed
title: IFsrmClassifierModuleDefinition::get_PropertiesUsed (fsrmpipeline.h)
description: The list of property names that the classifier inspects. (Get)
helpviewer_keywords: ["IFsrmClassifierModuleDefinition interface [File Server Resource Manager]","PropertiesUsed property","IFsrmClassifierModuleDefinition.PropertiesUsed","IFsrmClassifierModuleDefinition.get_PropertiesUsed","IFsrmClassifierModuleDefinition::PropertiesUsed","IFsrmClassifierModuleDefinition::get_PropertiesUsed","IFsrmClassifierModuleDefinition::put_PropertiesUsed","PropertiesUsed property [File Server Resource Manager]","PropertiesUsed property [File Server Resource Manager]","IFsrmClassifierModuleDefinition interface","fs.ifsrmclassifiermoduledefinition_propertiesused","fsrm.ifsrmclassifiermoduledefinition_propertiesused","fsrmpipeline/IFsrmClassifierModuleDefinition::PropertiesUsed","fsrmpipeline/IFsrmClassifierModuleDefinition::get_PropertiesUsed","fsrmpipeline/IFsrmClassifierModuleDefinition::put_PropertiesUsed","get_PropertiesUsed"]
old-location: fsrm\ifsrmclassifiermoduledefinition_propertiesused.htm
tech.root: fsrm
ms.assetid: 89bf8836-8d6d-41a1-a47c-ec92d2fd4a36
ms.date: 12/05/2018
ms.keywords: IFsrmClassifierModuleDefinition interface [File Server Resource Manager],PropertiesUsed property, IFsrmClassifierModuleDefinition.PropertiesUsed, IFsrmClassifierModuleDefinition.get_PropertiesUsed, IFsrmClassifierModuleDefinition::PropertiesUsed, IFsrmClassifierModuleDefinition::get_PropertiesUsed, IFsrmClassifierModuleDefinition::put_PropertiesUsed, PropertiesUsed property [File Server Resource Manager], PropertiesUsed property [File Server Resource Manager],IFsrmClassifierModuleDefinition interface, fs.ifsrmclassifiermoduledefinition_propertiesused, fsrm.ifsrmclassifiermoduledefinition_propertiesused, fsrmpipeline/IFsrmClassifierModuleDefinition::PropertiesUsed, fsrmpipeline/IFsrmClassifierModuleDefinition::get_PropertiesUsed, fsrmpipeline/IFsrmClassifierModuleDefinition::put_PropertiesUsed, get_PropertiesUsed
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
 - IFsrmClassifierModuleDefinition::get_PropertiesUsed
 - fsrmpipeline/IFsrmClassifierModuleDefinition::get_PropertiesUsed
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
 - IFsrmClassifierModuleDefinition.PropertiesUsed
 - IFsrmClassifierModuleDefinition.get_PropertiesUsed
 - IFsrmClassifierModuleDefinition.put_PropertiesUsed
---

# IFsrmClassifierModuleDefinition::get_PropertiesUsed


## -description

The list of property names that the classifier inspects.

This property is read/write.

## -parameters

## -remarks

The classifier may inspect the properties to determine the property value or if it should perform other processes.

The list is optional. Specify a list of properties only if you want to limit the properties that this classifier can inspect; otherwise, if the list is empty, the classifier can inspect any property in the file.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a>
