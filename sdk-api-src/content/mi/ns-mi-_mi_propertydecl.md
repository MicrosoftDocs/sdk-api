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

# _MI_PropertyDecl structure


## -description


Represents a class property (element) in a class's declaration.


## -struct-fields




### -field flags



#### MI_FLAG_PROPERTY ((1 << 2))

Indicates structure is a property.



#### MI_FLAG_KEY ((1 << 12))

Indicate structure is a key property.


### -field code

Hash code: (name[0] &lt;&lt; 16) | (name[len-1] &lt;&lt; 8) | len


### -field name

Name of this property.


### -field qualifiers

Qualifier set for this property.


### -field numQualifiers

Number of qualifiers.


### -field type

Type of  property.


### -field className

Name of reference class or embedded instance class name.


### -field subscript

If property is a fixed length array, then this value will hold the length of the array.


### -field offset

Offset of this property field from the start of the <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>.


### -field origin

Ancestor class that first defined a property with this name.


### -field propagator

Ancestor class that last defined a property with this name.


### -field value

Default value of this property.

