---
UID: NE:d2d1_1.D2D1_PROPERTY
title: D2D1_PROPERTY (d2d1_1.h)
description: Specifies the indices of the system properties present on the ID2D1Properties interface for an ID2D1Effect.
helpviewer_keywords: ["D2D1_PROPERTY","D2D1_PROPERTY","D2D1_PROPERTY enumeration [Direct2D]","D2D1_PROPERTY_AUTHOR","D2D1_PROPERTY_CACHED","D2D1_PROPERTY_CATEGORY","D2D1_PROPERTY_CLSID","D2D1_PROPERTY_DESCRIPTION","D2D1_PROPERTY_DISPLAYNAME","D2D1_PROPERTY_INPUTS","D2D1_PROPERTY_MAX_INPUTS","D2D1_PROPERTY_MIN_INPUTS","D2D1_PROPERTY_PRECISION","d2d1_1/D2D1_PROPERTY","d2d1_1/D2D1_PROPERTY_AUTHOR","d2d1_1/D2D1_PROPERTY_CACHED","d2d1_1/D2D1_PROPERTY_CATEGORY","d2d1_1/D2D1_PROPERTY_CLSID","d2d1_1/D2D1_PROPERTY_DESCRIPTION","d2d1_1/D2D1_PROPERTY_DISPLAYNAME","d2d1_1/D2D1_PROPERTY_INPUTS","d2d1_1/D2D1_PROPERTY_MAX_INPUTS","d2d1_1/D2D1_PROPERTY_MIN_INPUTS","d2d1_1/D2D1_PROPERTY_PRECISION","direct2d.__d2d1_property"]
old-location: direct2d\__d2d1_property.htm
tech.root: Direct2D
ms.assetid: 7261ea3c-bd52-4809-93c8-9e7a0a7424d0
ms.date: 12/05/2018
ms.keywords: D2D1_PROPERTY, D2D1_PROPERTY , D2D1_PROPERTY enumeration [Direct2D], D2D1_PROPERTY_AUTHOR, D2D1_PROPERTY_CACHED, D2D1_PROPERTY_CATEGORY, D2D1_PROPERTY_CLSID, D2D1_PROPERTY_DESCRIPTION, D2D1_PROPERTY_DISPLAYNAME, D2D1_PROPERTY_INPUTS, D2D1_PROPERTY_MAX_INPUTS, D2D1_PROPERTY_MIN_INPUTS, D2D1_PROPERTY_PRECISION, d2d1_1/D2D1_PROPERTY, d2d1_1/D2D1_PROPERTY_AUTHOR, d2d1_1/D2D1_PROPERTY_CACHED, d2d1_1/D2D1_PROPERTY_CATEGORY, d2d1_1/D2D1_PROPERTY_CLSID, d2d1_1/D2D1_PROPERTY_DESCRIPTION, d2d1_1/D2D1_PROPERTY_DISPLAYNAME, d2d1_1/D2D1_PROPERTY_INPUTS, d2d1_1/D2D1_PROPERTY_MAX_INPUTS, d2d1_1/D2D1_PROPERTY_MIN_INPUTS, d2d1_1/D2D1_PROPERTY_PRECISION, direct2d.__d2d1_property
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
req.typenames: D2D1_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_PROPERTY
 - d2d1_1/D2D1_PROPERTY
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
 - D2D1_PROPERTY
---

# D2D1_PROPERTY enumeration


## -description

Specifies the indices of the system properties present on the <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a> interface for an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>.

## -enum-fields

### -field D2D1_PROPERTY_CLSID:0x80000000

The CLSID of the effect.

### -field D2D1_PROPERTY_DISPLAYNAME:0x80000001

The name of the effect.

### -field D2D1_PROPERTY_AUTHOR:0x80000002

The author of the effect.

### -field D2D1_PROPERTY_CATEGORY:0x80000003

The category of the effect.

### -field D2D1_PROPERTY_DESCRIPTION:0x80000004

The description of the effect.

### -field D2D1_PROPERTY_INPUTS:0x80000005

The names of the effect's inputs.

### -field D2D1_PROPERTY_CACHED:0x80000006

The output of the effect should be cached.

### -field D2D1_PROPERTY_PRECISION:0x80000007

The buffer precision of the effect output.

### -field D2D1_PROPERTY_MIN_INPUTS:0x80000008

The minimum number of inputs supported by the effect.

### -field D2D1_PROPERTY_MAX_INPUTS:0x80000009

The maximum number of inputs supported by the effect.

### -field D2D1_PROPERTY_FORCE_DWORD:0xffffffff

## -remarks

Under normal circumstances the minimum and maximum number of inputs to the effect are the same. If the effect supports a variable number of inputs, the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1effect-setinputcount">ID2D1Effect::SetNumberOfInputs</a> method can be used to choose the number that the application will enable.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyname(uint32_pwstr_uint32)">ID2D1Properties::GetPropertyName</a>



[ID2D1Properties::GetPropertyNameLength](./nf-d2d1_1-id2d1properties-getpropertynamelength(u).md)



[ID2D1Properties::GetSubProperties](./nf-d2d1_1-id2d1properties-getsubproperties(u_id2d1properties).md)



<a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-gettype(u)">ID2D1Properties::GetType</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)">ID2D1Properties::GetValue</a>



<a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluesize(u)">ID2D1Properties::GetValueSize</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)">ID2D1Properties::SetValue</a>
