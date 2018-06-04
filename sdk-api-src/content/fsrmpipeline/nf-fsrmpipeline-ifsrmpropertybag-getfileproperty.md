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

# IFsrmPropertyBag::GetFileProperty


## -description


Retrieves the specified property from the property bag.


## -parameters




### -param name [in]

The name of the property to retrieve.


### -param fileProperty [out]

An <a href="https://msdn.microsoft.com/feffccd1-cf72-45c0-97b3-d6efd736223e">IFsrmProperty</a> interface to the retrieved property.


## -returns



The method returns the following return values.




## -remarks



Use the property name specified in the rule's <a href="https://msdn.microsoft.com/0e41ac2b-c48a-4bb8-a363-8a64c856b8f9">PropertyAffected</a> property.




## -see-also




<a href="https://msdn.microsoft.com/237f024d-2b1d-45d5-a63d-c530426278e6">IFsrmPropertyBag</a>



<a href="https://msdn.microsoft.com/d3322907-c832-49ef-bf21-2e4581251a88">IFsrmPropertyBag::SetFileProperty</a>
 

 

