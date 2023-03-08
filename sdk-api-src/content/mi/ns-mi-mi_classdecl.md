---
UID: NS:mi._MI_ClassDecl
title: MI_ClassDecl (mi.h)
description: This structure outlines the class declaration. It contains class name and hierarchy, properties, qualifiers, and methods.
helpviewer_keywords: ["MI_ClassDecl","MI_ClassDecl structure [Windows Management Infrastructure (MI)]","MI_FLAG_ABSTRACT","MI_FLAG_ASSOCIATION","MI_FLAG_CLASS","MI_FLAG_INDICATION","MI_FLAG_TERMINAL","mi/MI_ClassDecl","wmi_v2.mi_classdecl"]
old-location: wmi_v2\mi_classdecl.htm
tech.root: wmi_v2
ms.assetid: 8e2e2838-5d08-4e51-be96-0928042ccb9f
ms.date: 12/05/2018
ms.keywords: MI_ClassDecl, MI_ClassDecl structure [Windows Management Infrastructure (MI)], MI_FLAG_ABSTRACT, MI_FLAG_ASSOCIATION, MI_FLAG_CLASS, MI_FLAG_INDICATION, MI_FLAG_TERMINAL, mi/MI_ClassDecl, wmi_v2.mi_classdecl
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
req.typenames: MI_ClassDecl
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ClassDecl
 - mi/_MI_ClassDecl
 - MI_ClassDecl
 - mi/MI_ClassDecl
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
 - MI_ClassDecl
---

# MI_ClassDecl structure


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

### -field numQualifiers

Length of <b>qualifiers</b> array.

### -field properties

The properties of this object.

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

### -field numMethods

Number of  methods in this class.

### -field schema

Pointer to schema this class belongs to.

### -field providerFT

Provider functions.

### -field owningClass

Owning <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> object, if any.
