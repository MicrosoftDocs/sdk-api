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

# _MI_MethodDecl structure


## -description


Represents a CIM method.


## -struct-fields




### -field flags

Flags:

<a id="MI_FLAG_METHOD"></a>
<a id="mi_flag_method"></a>


#### MI_FLAG_METHOD

<a id="MI_FLAG_STATIC"></a>
<a id="mi_flag_static"></a>


#### MI_FLAG_STATIC


### -field code

Hash code: <code>(name[0] &lt;&lt; 16) | (name[len-1] &lt;&lt; 8) | len</code>


### -field name

The method name.


### -field qualifiers

The qualifiers of the method.


### -field _MI_Qualifier

 


### -field numQualifiers

The number of qualifiers.


### -field parameters

The parameters of the method.


### -field _MI_ParameterDecl

 


### -field numParameters

The number of parameters.


### -field size

The size of the structure.


### -field returnType

The post result type of this method.


### -field origin

The ancestor class that first defined a method with this name.


### -field propagator

The ancestor class that last defined a method with this name.


### -field schema

The schema this class belongs to.


### -field _MI_SchemaDecl

 


### -field function

The extrinsic function that implements this method.


## -see-also




<a href="https://msdn.microsoft.com/7C669B89-C6D7-45E5-AAD8-A884F4E87659">MI_FeatureDecl</a>



<a href="https://msdn.microsoft.com/E35A291C-AB4F-4DF4-948E-14D1AF11D2FE">MI_MethodDecl_Invoke</a>



<a href="https://msdn.microsoft.com/09ad6ea4-09ae-428b-9df9-414043044d6a">MI_ParameterDecl</a>



<a href="https://msdn.microsoft.com/4BEBE8AB-90D3-4BBA-A544-7722309160A1">MI_Qualifier</a>



<a href="https://msdn.microsoft.com/70f1a14e-abd4-43e9-a7b4-fa00e07a125c">MI_SchemaDecl</a>
 

 

