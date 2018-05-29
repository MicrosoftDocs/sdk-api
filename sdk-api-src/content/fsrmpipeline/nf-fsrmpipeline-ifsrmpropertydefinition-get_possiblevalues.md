---
UID: NF:fsrmpipeline.IFsrmPropertyDefinition.get_PossibleValues
title: IFsrmPropertyDefinition::get_PossibleValues
author: windows-sdk-content
description: The possible values to which the property can be set.
old-location: fsrm\ifsrmpropertydefinition_possiblevalues.htm
old-project: Fsrm
ms.assetid: b48dd022-3c8d-41cb-aab5-18d24cad4521
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmPropertyDefinition interface [File Server Resource Manager],PossibleValues property, IFsrmPropertyDefinition.PossibleValues, IFsrmPropertyDefinition.get_PossibleValues, IFsrmPropertyDefinition::PossibleValues, IFsrmPropertyDefinition::get_PossibleValues, IFsrmPropertyDefinition::put_PossibleValues, PossibleValues property [File Server Resource Manager], PossibleValues property [File Server Resource Manager],IFsrmPropertyDefinition interface, fs.ifsrmpropertydefinition_possiblevalues, fsrm.ifsrmpropertydefinition_possiblevalues, fsrmpipeline/IFsrmPropertyDefinition::PossibleValues, fsrmpipeline/IFsrmPropertyDefinition::get_PossibleValues, fsrmpipeline/IFsrmPropertyDefinition::put_PossibleValues, get_PossibleValues
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmPropertyDefinition.PossibleValues
-	IFsrmPropertyDefinition.get_PossibleValues
-	IFsrmPropertyDefinition.put_PossibleValues
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmPropertyDefinition::get_PossibleValues


## -description


The possible values to which the property can be set.

This property is read/write.


## -parameters


## -remarks



You must specify a possible values list if the property's type is 
    <b>FsrmPropertyDefinitionType_OrderedList</b> or 
    <b>FsrmPropertyDefinitionType_MultiChoiceList.</b>

You cannot delete a possible value from the list if a rule specifies the value (see 
    <a href="https://msdn.microsoft.com/c243cf7a-23f5-4d81-acea-9bf6ed66967d">IFsrmClassificationRule.Value</a>). Deleting 
    the value does not remove the value from files that are currently classified using that value.

You can change the order of the values in the list. For ordered lists, changing the order can affect 
    aggregation the next time classification runs.

To specify descriptions for each possible value, set the 
    <a href="https://msdn.microsoft.com/3c6a9457-c1bb-4bc3-853a-3676bb4ce6bb">IFsrmPropertyDefinition.ValueDescriptions</a> 
    property.




## -see-also




<a href="https://msdn.microsoft.com/b85d5df0-a99a-48d2-9bad-3b8c86abea91">IFsrmPropertyDefinition</a>
 

 

