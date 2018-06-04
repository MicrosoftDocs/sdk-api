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
 

 

