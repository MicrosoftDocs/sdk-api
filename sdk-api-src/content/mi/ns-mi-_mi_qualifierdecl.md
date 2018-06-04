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

# _MI_QualifierDecl structure


## -description


Represents a CIM qualifier declaration.


## -struct-fields




### -field name

Name of this qualifier.


### -field type

Type of this qualifier.


### -field scope

Scope of this qualifier.


### -field flavor

Flavor of this qualifier. The flavor value may contain  any combination of these bit flags:



#### MI_FLAG_ENABLEOVERRIDE (0x00000080)

Enables override.



#### MI_FLAG_DISABLEOVERRIDE (0x00000100)

Disables override.



#### MI_FLAG_RESTRICTED (0x00000200)

Applies only to the class in which it is declared.



#### MI_FLAG_TOSUBCLASS (0x00000400)

Allows inheritance to any subclass.



#### MI_FLAG_TRANSLATABLE (0x00000800)

Allows for string localization.


### -field subscript

Array subscript. If this is an array type with a fixed length, the subscript value represents the array length.


### -field value

Pointer to a qualifier value of a particular type.

