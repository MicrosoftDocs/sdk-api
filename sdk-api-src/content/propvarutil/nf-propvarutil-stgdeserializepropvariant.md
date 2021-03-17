---
UID: NF:propvarutil.StgDeserializePropVariant
title: StgDeserializePropVariant function (propvarutil.h)
description: The StgDeserializePropVariant function converts a SERIALIZEDPROPERTYVALUE data type to a PROPVARIANT data type.
helpviewer_keywords: ["StgDeserializePropVariant","StgDeserializePropVariant function [Structured Storage]","propvarutil/StgDeserializePropVariant","stg.stgdeserializepropvariant"]
old-location: stg\stgdeserializepropvariant.htm
tech.root: Stg
ms.assetid: 55b4de40-d81d-4989-8f57-a286815fa495
ms.date: 12/05/2018
ms.keywords: StgDeserializePropVariant, StgDeserializePropVariant function [Structured Storage], propvarutil/StgDeserializePropVariant, stg.stgdeserializepropvariant
req.header: propvarutil.h
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
req.lib: Propsys.lib
req.dll: Propsys.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StgDeserializePropVariant
 - propvarutil/StgDeserializePropVariant
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - StgDeserializePropVariant
---

# StgDeserializePropVariant function


## -description

The <b>StgDeserializePropVariant</b> function converts a SERIALIZEDPROPERTYVALUE data type to a PROPVARIANT data type.

## -parameters

### -param pprop [in]

A pointer to the  <b>SERIALIZEDPROPERTYVALUE</b> buffer.

### -param cbMax [in]

The size of the <i>pprop</i> buffer in bytes.

### -param ppropvar [out]

A pointer to a <b>PROPVARIANT</b>.

## -returns

This function can return one of these values.

## -remarks

This function deserializes a <b>PROPVARIANT</b> data type. This function is similar to the <a href="/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant">StgConvertPropertyToVariant</a> function. The <b>StgDeserializePropVariant</b> function uses the default value of <b>CP_WINUNICODE</b> for the code page and a system provided allocator that uses task memory.  Use <b>StgDeserializePropVariant</b> unless you want to specify which code page and memory allocator to use.

## -see-also

<a href="/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant">StgConvertPropertyToVariant</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant">StgSerializePropVariant</a>