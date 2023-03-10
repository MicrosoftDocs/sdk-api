---
UID: NS:mi._MI_QualifierDecl
title: MI_QualifierDecl (mi.h)
description: Represents a CIM qualifier declaration.
helpviewer_keywords: ["MI_FLAG_DISABLEOVERRIDE","MI_FLAG_ENABLEOVERRIDE","MI_FLAG_RESTRICTED","MI_FLAG_TOSUBCLASS","MI_FLAG_TRANSLATABLE","MI_QualifierDecl","MI_QualifierDecl structure [Windows Management Infrastructure (MI)]","mi/MI_QualifierDecl","wmi._mi_qualifierdecl","wmi_v2.mi_qualifierdecl"]
old-location: wmi_v2\mi_qualifierdecl.htm
tech.root: wmi_v2
ms.assetid: 88d167f5-3cb0-41ed-9355-ea31ff263a03
ms.date: 12/05/2018
ms.keywords: MI_FLAG_DISABLEOVERRIDE, MI_FLAG_ENABLEOVERRIDE, MI_FLAG_RESTRICTED, MI_FLAG_TOSUBCLASS, MI_FLAG_TRANSLATABLE, MI_QualifierDecl, MI_QualifierDecl structure [Windows Management Infrastructure (MI)], mi/MI_QualifierDecl, wmi._mi_qualifierdecl, wmi_v2.mi_qualifierdecl
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
req.typenames: MI_QualifierDecl
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_QualifierDecl
 - mi/_MI_QualifierDecl
 - MI_QualifierDecl
 - mi/MI_QualifierDecl
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
 - MI_QualifierDecl
---

# MI_QualifierDecl structure


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

