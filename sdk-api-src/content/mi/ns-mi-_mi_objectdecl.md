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

# _MI_ObjectDecl structure


## -description


Contains properties common to the <a href="https://msdn.microsoft.com/8e2e2838-5d08-4e51-be96-0928042ccb9f">MI_ClassDecl</a> and <a href="https://msdn.microsoft.com/bc5e5c1e-3483-4762-8063-047308dc3652">MI_PropertyDecl</a> structures. It can be used to write functions
that work on the common fields of these two types.


## -struct-fields




### -field flags

Flags.


### -field code

Hash code.


### -field name

Name of this feature.


### -field qualifiers

Describes metadata for classes and properties.


### -field numQualifiers

Length of <b>qualifiers</b> array.


### -field properties

The properties of this object.


### -field _MI_PropertyDecl

 


### -field numProperties

The number of properties of this object.


### -field size

Size of the structure.


## -see-also




<a href="https://msdn.microsoft.com/8e2e2838-5d08-4e51-be96-0928042ccb9f">MI_ClassDecl</a>



<a href="https://msdn.microsoft.com/7C669B89-C6D7-45E5-AAD8-A884F4E87659">MI_FeatureDecl</a>



<a href="https://msdn.microsoft.com/bc5e5c1e-3483-4762-8063-047308dc3652">MI_PropertyDecl</a>



<a href="https://msdn.microsoft.com/4BEBE8AB-90D3-4BBA-A544-7722309160A1">MI_Qualifier</a>
 

 

