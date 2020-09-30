---
UID: NS:mi._MI_ObjectDecl
title: MI_ObjectDecl (mi.h)
description: Contains properties common to the MI_ClassDecl and MI_PropertyDecl structures.
helpviewer_keywords: ["MI_ObjectDecl","MI_ObjectDecl structure [Windows Management Infrastructure (MI)]","mi/MI_ObjectDecl","wmi_v2.mi_objectdecl"]
old-location: wmi_v2\mi_objectdecl.htm
tech.root: wmi_v2
ms.assetid: 8759FEE5-9703-443E-9A2D-982158BC2EFA
ms.date: 12/05/2018
ms.keywords: MI_ObjectDecl, MI_ObjectDecl structure [Windows Management Infrastructure (MI)], mi/MI_ObjectDecl, wmi_v2.mi_objectdecl
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
targetos: Windows
req.typenames: MI_ObjectDecl
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ObjectDecl
 - mi/_MI_ObjectDecl
 - MI_ObjectDecl
 - mi/MI_ObjectDecl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_ObjectDecl
---

# MI_ObjectDecl structure


## -description

Contains properties common to the <a href="/windows/desktop/api/mi/ns-mi-mi_classdecl">MI_ClassDecl</a> and <a href="/windows/desktop/api/mi/ns-mi-mi_propertydecl">MI_PropertyDecl</a> structures. It can be used to write functions
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

<a href="/windows/desktop/api/mi/ns-mi-mi_classdecl">MI_ClassDecl</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_featuredecl">MI_FeatureDecl</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_propertydecl">MI_PropertyDecl</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_qualifier">MI_Qualifier</a>