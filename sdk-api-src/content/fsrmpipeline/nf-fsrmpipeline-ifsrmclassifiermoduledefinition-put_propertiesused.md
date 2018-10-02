---
UID: NF:fsrmpipeline.IFsrmClassifierModuleDefinition.put_PropertiesUsed
title: IFsrmClassifierModuleDefinition::put_PropertiesUsed
author: windows-sdk-content
description: The list of property names that the classifier inspects.
old-location: fsrm\ifsrmclassifiermoduledefinition_propertiesused.htm
tech.root: Fsrm
ms.assetid: 89bf8836-8d6d-41a1-a47c-ec92d2fd4a36
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFsrmClassifierModuleDefinition interface [File Server Resource Manager],PropertiesUsed property, IFsrmClassifierModuleDefinition.PropertiesUsed, IFsrmClassifierModuleDefinition.put_PropertiesUsed, IFsrmClassifierModuleDefinition::PropertiesUsed, IFsrmClassifierModuleDefinition::get_PropertiesUsed, IFsrmClassifierModuleDefinition::put_PropertiesUsed, PropertiesUsed property [File Server Resource Manager], PropertiesUsed property [File Server Resource Manager],IFsrmClassifierModuleDefinition interface, fs.ifsrmclassifiermoduledefinition_propertiesused, fsrm.ifsrmclassifiermoduledefinition_propertiesused, fsrmpipeline/IFsrmClassifierModuleDefinition::PropertiesUsed, fsrmpipeline/IFsrmClassifierModuleDefinition::get_PropertiesUsed, fsrmpipeline/IFsrmClassifierModuleDefinition::put_PropertiesUsed, put_PropertiesUsed
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
 - IFsrmClassifierModuleDefinition.PropertiesUsed
 - IFsrmClassifierModuleDefinition.get_PropertiesUsed
 - IFsrmClassifierModuleDefinition.put_PropertiesUsed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassifierModuleDefinition::put_PropertiesUsed


## -description


The list of property names that the classifier inspects.

This property is read/write.


## -parameters


## -remarks



The classifier may inspect the properties to determine the property value or if it should perform other processes.

The list is optional. Specify a list of properties only if you want to limit the properties that this classifier can inspect; otherwise, if the list is empty, the classifier can inspect any property in the file.




## -see-also




<a href="https://msdn.microsoft.com/6e691670-d7d7-48cb-8a81-ee8828b39b30">IFsrmClassifierModuleDefinition</a>
 

 

