---
UID: NE:d2d1_1.D2D1_SUBPROPERTY
title: D2D1_SUBPROPERTY (d2d1_1.h)
description: Specifies the indices of the system sub-properties that may be present in any property.
helpviewer_keywords: ["D2D1_SUBPROPERTY","D2D1_SUBPROPERTY enumeration [Direct2D]","D2D1_SUBPROPERTY_DEFAULT","D2D1_SUBPROPERTY_DISPLAYNAME","D2D1_SUBPROPERTY_FIELDS","D2D1_SUBPROPERTY_INDEX","D2D1_SUBPROPERTY_ISREADONLY","D2D1_SUBPROPERTY_MAX","D2D1_SUBPROPERTY_MIN","d2d1_1/D2D1_SUBPROPERTY","d2d1_1/D2D1_SUBPROPERTY_DEFAULT","d2d1_1/D2D1_SUBPROPERTY_DISPLAYNAME","d2d1_1/D2D1_SUBPROPERTY_FIELDS","d2d1_1/D2D1_SUBPROPERTY_INDEX","d2d1_1/D2D1_SUBPROPERTY_ISREADONLY","d2d1_1/D2D1_SUBPROPERTY_MAX","d2d1_1/D2D1_SUBPROPERTY_MIN","direct2d.__d2d1_subproperty"]
old-location: direct2d\__d2d1_subproperty.htm
tech.root: Direct2D
ms.assetid: 311a1b6f-ef0e-4453-a5fe-d06ebb0bb222
ms.date: 12/05/2018
ms.keywords: D2D1_SUBPROPERTY, D2D1_SUBPROPERTY enumeration [Direct2D], D2D1_SUBPROPERTY_DEFAULT, D2D1_SUBPROPERTY_DISPLAYNAME, D2D1_SUBPROPERTY_FIELDS, D2D1_SUBPROPERTY_INDEX, D2D1_SUBPROPERTY_ISREADONLY, D2D1_SUBPROPERTY_MAX, D2D1_SUBPROPERTY_MIN, d2d1_1/D2D1_SUBPROPERTY, d2d1_1/D2D1_SUBPROPERTY_DEFAULT, d2d1_1/D2D1_SUBPROPERTY_DISPLAYNAME, d2d1_1/D2D1_SUBPROPERTY_FIELDS, d2d1_1/D2D1_SUBPROPERTY_INDEX, d2d1_1/D2D1_SUBPROPERTY_ISREADONLY, d2d1_1/D2D1_SUBPROPERTY_MAX, d2d1_1/D2D1_SUBPROPERTY_MIN, direct2d.__d2d1_subproperty
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: D2D1_SUBPROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SUBPROPERTY
 - d2d1_1/D2D1_SUBPROPERTY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D2d1_1.h
api_name:
 - D2D1_SUBPROPERTY
---

# D2D1_SUBPROPERTY enumeration


## -description

Specifies the indices of the system sub-properties that may be present in any property.

## -enum-fields

### -field D2D1_SUBPROPERTY_DISPLAYNAME:0x80000000

The name for the parent property.

### -field D2D1_SUBPROPERTY_ISREADONLY:0x80000001

A Boolean indicating whether the parent property is writable.

### -field D2D1_SUBPROPERTY_MIN:0x80000002

The minimum value that can be set to the parent property.

### -field D2D1_SUBPROPERTY_MAX:0x80000003

The maximum value that can be set to the parent property.

### -field D2D1_SUBPROPERTY_DEFAULT:0x80000004

The default value of the parent property.

### -field D2D1_SUBPROPERTY_FIELDS:0x80000005

An array of name/index pairs that indicate the possible values that can be set to the parent property.

### -field D2D1_SUBPROPERTY_INDEX:0x80000006

An index sub-property used by the elements of the <b>D2D1_SUBPROPERTY_FIELDS</b> array.

### -field D2D1_SUBPROPERTY_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyname(uint32_pwstr_uint32)">ID2D1Properties::GetPropertyName</a>



[ID2D1Properties::GetPropertyNameLength](./nf-d2d1_1-id2d1properties-getpropertynamelength(u).md)



[ID2D1Properties::GetSubProperties](./nf-d2d1_1-id2d1properties-getsubproperties(u_id2d1properties).md)



<a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-gettype(u)">ID2D1Properties::GetType</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)">ID2D1Properties::GetValue</a>



<a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluesize(u)">ID2D1Properties::GetValueSize</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)">ID2D1Properties::SetValue</a>
