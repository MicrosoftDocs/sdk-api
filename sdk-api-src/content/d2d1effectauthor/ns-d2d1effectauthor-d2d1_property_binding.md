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

# D2D1_PROPERTY_BINDING structure


## -description


Defines a property binding to a pair of functions which get and set the corresponding property. 


## -struct-fields




### -field propertyName

 The name of the property.


### -field setFunction

 The function that will receive the data to set.


### -field getFunction

The function that will be asked to write the output data.


## -remarks



The <b>propertyName</b> is used to cross-correlate the property binding with the registration XML. The <b>propertyName</b> must be present in the XML call or the registration will fail.



All properties must be bound.




## -see-also




<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>



<a href="https://msdn.microsoft.com/9988aad6-0487-4f48-a05c-1dfb944f6ce7">ID2D1Factory::RegisterEffect</a>
 

 

