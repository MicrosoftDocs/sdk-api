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

# PROPERTYORIGIN enumeration


## -description


Returned by <a href="https://msdn.microsoft.com/6b7f298c-1b3d-463d-a5ec-fbe72672ef49">GetThemePropertyOrigin</a> to specify where a property was found.


## -enum-fields




### -field PO_STATE

Property was found in the state section.


### -field PO_PART

Property was found in the part section.


### -field PO_CLASS

Property was found in the class section.


### -field PO_GLOBAL

Property was found in the list of global variables. 


### -field PO_NOTFOUND

Property was not found.


## -see-also




<a href="https://msdn.microsoft.com/6b7f298c-1b3d-463d-a5ec-fbe72672ef49">GetThemePropertyOrigin</a>
 

 

