---
UID: NF:propidl.StgConvertVariantToProperty
title: StgConvertVariantToProperty function (propidl.h)
description: Converts a PROPVARIANT data type to a SERIALIZEDPROPERTYVALUE data type.
helpviewer_keywords: ["StgConvertVariantToProperty","StgConvertVariantToProperty function [Structured Storage]","propidl/StgConvertVariantToProperty","stg.stgconvertvarianttoproperty"]
old-location: stg\stgconvertvarianttoproperty.htm
tech.root: Stg
ms.assetid: 3d35b808-4fa6-44ec-9c46-96ceee1dafd0
ms.date: 12/05/2018
ms.keywords: StgConvertVariantToProperty, StgConvertVariantToProperty function [Structured Storage], propidl/StgConvertVariantToProperty, stg.stgconvertvarianttoproperty
req.header: propidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StgConvertVariantToProperty
 - propidl/StgConvertVariantToProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - StgConvertVariantToProperty
---

# StgConvertVariantToProperty function


## -description

The <b>StgConvertVariantToProperty</b> function converts a <b>PROPVARIANT</b> data type to a <b>SERIALIZEDPROPERTYVALUE</b> data type.

## -parameters

### -param pvar [in]

A  pointer to <b>PROPVARIANT</b>.

### -param CodePage [in]

A property set codepage.

### -param pprop [out, optional]

Optional. A pointer to <b>SERIALIZEDPROPERTYVALUE</b>.

### -param pcb [in, out]

A pointer to the remaining stream length, updated to the actual property size on return.

### -param pid [in]

The propid (used if indirect).

### -param fReserved [in]

Reserver. The value must be <b>FALSE</b>.

### -param pcIndirect [in, out, optional]

Optional. A pointer to the indirect property count.

## -returns

Returns a pointer to <b>SERIALIZEDPROPERTYVALUE</b>.

## -remarks

This function converts a <b>PROPVARIANT</b> to a property. If the function fails it throws an exception that represents <b>STATUS_INVALID_PARAMETER NT_STATUS</b>.

## -see-also

<a href="/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant">StgConvertPropertyToVariant</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant">StgSerializePropVariant</a>