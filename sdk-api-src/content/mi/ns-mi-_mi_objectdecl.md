---
UID: NS:mi._MI_ObjectDecl
title: "_MI_ObjectDecl"
author: windows-sdk-content
description: Contains properties common to the MI_ClassDecl and MI_PropertyDecl structures.
old-location: wmi_v2\mi_objectdecl.htm
old-project: wmi_v2
ms.assetid: 8759FEE5-9703-443E-9A2D-982158BC2EFA
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_ObjectDecl, MI_ObjectDecl structure [Windows Management Infrastructure (MI)], _MI_ObjectDecl, mi/MI_ObjectDecl, wmi_v2.mi_objectdecl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
tech.root: 
req.typenames: MI_ObjectDecl
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_ObjectDecl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

