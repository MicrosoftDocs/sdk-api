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

# _MI_ClassDecl structure


## -description


This structure outlines the class declaration.  It contains class name and hierarchy, properties, qualifiers, and methods.


## -struct-fields




### -field flags

Flags can consist of values from following list.



#### MI_FLAG_CLASS ((1 << 0))

Indicates the structure describes a class.



#### MI_FLAG_ASSOCIATION ((1 << 4))

Indicates the class is also an association class.



#### MI_FLAG_INDICATION ((1 << 5))

Indicates the class is also an indication class.



#### MI_FLAG_ABSTRACT ((1 << 17))

Indicates the class is abstract.



#### MI_FLAG_TERMINAL ((1 << 18))

Indicates class cannot be derived from.


### -field code

Hash code: (name[0] &lt;&lt; 16) | (name[len-1] &lt;&lt; 8) | len


### -field name

Name of this feature.


### -field qualifiers

Describes extra metadata for classes, properties, methods, and parameters.


### -field _MI_Qualifier

 


### -field numQualifiers

Length of <b>qualifiers</b> array.


### -field properties

The properties of this object.


### -field _MI_PropertyDecl

 


### -field numProperties

The number of properties of this object.


### -field size

Size of structure described by <b>MI_ClassDecl</b>.


### -field superClass

Parent class name.


### -field superClassDecl

The classDecl for the parent class <b>superClass</b>.


### -field methods

The methods of this class.


### -field _MI_MethodDecl

 


### -field numMethods

Number of  methods in this class.


### -field schema

Pointer to schema this class belongs to.


### -field _MI_SchemaDecl

 


### -field providerFT

Provider functions.


### -field owningClass

Owning <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> object, if any.

