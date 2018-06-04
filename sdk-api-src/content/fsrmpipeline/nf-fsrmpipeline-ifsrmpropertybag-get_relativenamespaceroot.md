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

# IFsrmPropertyBag::get_RelativeNamespaceRoot


## -description


The relative path of the namespace root under which the file is being evaluated.

This property is read-only.


## -parameters


## -remarks



This property is only valid under an evaluation context. Classifier modules that retrieve this property will get the namespace root of the rule under which the file is being evaluated. Because storage modules do not have evaluation contexts, they must not retrieve this property.

The relative namespace root is the path of the namespace root relative to the volume root.  For example, if the path to the file is "P:\folder1\subfolderA\test.txt", and the file is being evaluated by a rule with a namespace root of "P:\folder1", then the relative namespace root would be "\folder1\". Note that the rule's namespace root determines the relative namespace root.

The caller should not expect that the relative namespace root returned will consistently have leading or trailing backslashes.




## -see-also




<a href="https://msdn.microsoft.com/237f024d-2b1d-45d5-a63d-c530426278e6">IFsrmPropertyBag</a>
 

 

