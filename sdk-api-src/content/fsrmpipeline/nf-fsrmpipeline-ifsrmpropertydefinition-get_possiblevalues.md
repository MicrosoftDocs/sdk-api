---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

