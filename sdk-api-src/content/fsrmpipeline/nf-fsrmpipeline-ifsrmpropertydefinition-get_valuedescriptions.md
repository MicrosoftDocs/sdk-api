---
UID: NF:fsrmpipeline.IFsrmPropertyDefinition.get_ValueDescriptions
title: IFsrmPropertyDefinition::get_ValueDescriptions
author: windows-sdk-content
description: Descriptions for each of the possible values specified in the PossibleValues property.
old-location: fsrm\ifsrmpropertydefinition_valuedescriptions.htm
tech.root: fsrm
ms.assetid: 3c6a9457-c1bb-4bc3-853a-3676bb4ce6bb
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IFsrmPropertyDefinition interface [File Server Resource Manager],ValueDescriptions property, IFsrmPropertyDefinition.ValueDescriptions, IFsrmPropertyDefinition.get_ValueDescriptions, IFsrmPropertyDefinition::ValueDescriptions, IFsrmPropertyDefinition::get_ValueDescriptions, IFsrmPropertyDefinition::put_ValueDescriptions, ValueDescriptions property [File Server Resource Manager], ValueDescriptions property [File Server Resource Manager],IFsrmPropertyDefinition interface, fs.ifsrmpropertydefinition_valuedescriptions, fsrm.ifsrmpropertydefinition_valuedescriptions, fsrmpipeline/IFsrmPropertyDefinition::ValueDescriptions, fsrmpipeline/IFsrmPropertyDefinition::get_ValueDescriptions, fsrmpipeline/IFsrmPropertyDefinition::put_ValueDescriptions, get_ValueDescriptions
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
 - IFsrmPropertyDefinition.ValueDescriptions
 - IFsrmPropertyDefinition.get_ValueDescriptions
 - IFsrmPropertyDefinition.put_ValueDescriptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmPropertyDefinition::get_ValueDescriptions


## -description


Descriptions for each of the possible values specified in the 
    <a href="https://msdn.microsoft.com/b48dd022-3c8d-41cb-aab5-18d24cad4521">PossibleValues</a> 
    property.

This property is read/write.


## -parameters


## -remarks



There is a one-to-one relationship between these descriptions and the list of possible values specified in the 
    <a href="https://msdn.microsoft.com/b48dd022-3c8d-41cb-aab5-18d24cad4521">PossibleValues</a> property. If you 
    do not want to specify a description for one of the values in the list, set the corresponding item in the array to 
    an empty string.




## -see-also




<a href="https://msdn.microsoft.com/b85d5df0-a99a-48d2-9bad-3b8c86abea91">IFsrmPropertyDefinition</a>
 

 

