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

# DSQUERYCLASSLIST structure


## -description


The <b>DSQUERYCLASSLIST</b> structure describes a list of classes against which a directory service query is made.


## -struct-fields




### -field cbStruct

Size, in bytes, of this structure.


### -field cClasses

Number of the classes in the array.


### -field offsetClass

Offset to the class names of Unicode strings.


## -remarks



The class list is retrieved by the form pages upon receiving a DSQPM_GETCLASSLIST page message.




## -see-also




<a href="https://msdn.microsoft.com/bf6aa066-ee7e-4b13-9a4b-1e097632ec5a">Active
  Directory Display Structures</a>
 

 

