---
UID: NS:mi._MI_PropertyDecl
title: MI_PropertyDecl (mi.h)
description: Represents a class property (element) in a class's declaration.
helpviewer_keywords: ["MI_FLAG_KEY","MI_FLAG_PROPERTY","MI_PropertyDecl","MI_PropertyDecl structure [Windows Management Infrastructure (MI)]","mi/MI_PropertyDecl","wmi._mi_propertydecl","wmi_v2.mi_propertydecl"]
old-location: wmi_v2\mi_propertydecl.htm
tech.root: wmi_v2
ms.assetid: bc5e5c1e-3483-4762-8063-047308dc3652
ms.date: 12/05/2018
ms.keywords: MI_FLAG_KEY, MI_FLAG_PROPERTY, MI_PropertyDecl, MI_PropertyDecl structure [Windows Management Infrastructure (MI)], mi/MI_PropertyDecl, wmi._mi_propertydecl, wmi_v2.mi_propertydecl
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
req.typenames: MI_PropertyDecl
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_PropertyDecl
 - mi/_MI_PropertyDecl
 - MI_PropertyDecl
 - mi/MI_PropertyDecl
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
 - MI_PropertyDecl
---

# MI_PropertyDecl structure


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

Offset of this property field from the start of the <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a>.

### -field origin

Ancestor class that first defined a property with this name.

### -field propagator

Ancestor class that last defined a property with this name.

### -field value

Default value of this property.