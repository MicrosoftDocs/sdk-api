---
UID: NS:mi._MI_MethodDecl
title: "_MI_MethodDecl"
author: windows-sdk-content
description: Represents a CIM method.
old-location: wmi_v2\mi_methoddecl.htm
tech.root: WMI_v2
ms.assetid: 50087394-44C2-4CE5-8952-9795FE9B236A
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_FLAG_METHOD, MI_FLAG_STATIC, MI_MethodDecl, MI_MethodDecl structure [Windows Management Infrastructure (MI)], _MI_MethodDecl, mi/MI_MethodDecl, wmi_v2.mi_methoddecl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_MethodDecl
product: Windows
targetos: Windows
req.typenames: MI_MethodDecl
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
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
 

 

