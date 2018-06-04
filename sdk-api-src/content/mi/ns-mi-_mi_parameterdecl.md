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

# _MI_ParameterDecl structure


## -description


Represents CIM method parameters.


## -struct-fields




### -field flags

flags



#### MI_FLAG_PROPERTY ((1 << 2))

Indicates structure is a property.


### -field code

Hash code: (name[0] &lt;&lt; 16) | (name[len-1] &lt;&lt; 8) | len


### -field name

Name of this parameter.


### -field qualifiers

Set of qualifiers for this parameter.


### -field numQualifiers

Number of parameter qualifiers.


### -field type

Type of  parameter.


### -field className

Name of reference class or strongly typed embedded instance.


### -field subscript

If the parameter is an array type of a fixed length, this value holds the subscript value.


### -field offset

Offset from the start of the instance of where the value field of this parameter will exist.

