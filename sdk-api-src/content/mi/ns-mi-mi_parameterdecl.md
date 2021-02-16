---
UID: NS:mi._MI_ParameterDecl
title: MI_ParameterDecl (mi.h)
description: Represents CIM method parameters.
helpviewer_keywords: ["MI_FLAG_PROPERTY","MI_ParameterDecl","MI_ParameterDecl structure [Windows Management Infrastructure (MI)]","mi/MI_ParameterDecl","wmi._mi_parameterdecl","wmi_v2.mi_parameterdecl"]
old-location: wmi_v2\mi_parameterdecl.htm
tech.root: wmi_v2
ms.assetid: 09ad6ea4-09ae-428b-9df9-414043044d6a
ms.date: 12/05/2018
ms.keywords: MI_FLAG_PROPERTY, MI_ParameterDecl, MI_ParameterDecl structure [Windows Management Infrastructure (MI)], mi/MI_ParameterDecl, wmi._mi_parameterdecl, wmi_v2.mi_parameterdecl
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
req.typenames: MI_ParameterDecl
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ParameterDecl
 - mi/_MI_ParameterDecl
 - MI_ParameterDecl
 - mi/MI_ParameterDecl
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
 - MI_ParameterDecl
---

# MI_ParameterDecl structure


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

