---
UID: NE:medparam._MP_Type
title: MP_TYPE (medparam.h)
description: The MP_TYPE enumeration specifies the data type for a parameter.
helpviewer_keywords: ["MPT_BOOL","MPT_ENUM","MPT_FLOAT","MPT_INT","MPT_MAX","MP_TYPE","MP_TYPE","MP_TYPE enumeration [DirectShow]","MP_TYPEEnumeration","dshow.mp_type","medparam/MPT_BOOL","medparam/MPT_ENUM","medparam/MPT_FLOAT","medparam/MPT_INT","medparam/MPT_MAX","medparam/MP_TYPE"]
old-location: dshow\mp_type.htm
tech.root: dshow
ms.assetid: 9c8851c7-1a72-4dfd-ba2f-e64d8e22f6dc
ms.date: 12/05/2018
ms.keywords: MPT_BOOL, MPT_ENUM, MPT_FLOAT, MPT_INT, MPT_MAX, MP_TYPE, MP_TYPE , MP_TYPE enumeration [DirectShow], MP_TYPEEnumeration, dshow.mp_type, medparam/MPT_BOOL, medparam/MPT_ENUM, medparam/MPT_FLOAT, medparam/MPT_INT, medparam/MPT_MAX, medparam/MP_TYPE
req.header: medparam.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MP_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MP_Type
 - medparam/_MP_Type
 - MP_TYPE
 - medparam/MP_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Medparam.h
api_name:
 - MP_TYPE
---

# MP_TYPE enumeration


## -description

The <code>MP_TYPE</code> enumeration specifies the data type for a parameter.

## -enum-fields

### -field MPT_INT:0

Value is a signed 32-bit integer.

### -field MPT_FLOAT

Value is a 32-bit IEEE floating-point value.

### -field MPT_BOOL

Value is Boolean. Use the following constants for Boolean parameters:

### -field MPT_ENUM

Value is taken from a set of consecutive integers.

### -field MPT_MAX

Reserved.

## -remarks

To reduce type conversions at run time, all parameters have 32-bit float values, defined as type <b>MP_DATA</b>. The members of this enumeration specify how a given parameter should be interpreted.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/previous-versions/windows/desktop/api/medparam/ns-medparam-mp_paraminfo">MP_PARAMINFO</a>
