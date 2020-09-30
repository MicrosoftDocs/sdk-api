---
UID: NF:propidl.StgConvertPropertyToVariant
title: StgConvertPropertyToVariant function (propidl.h)
description: Converts a SERIALIZEDPROPERTYVALUE data type to a PROPVARIANT data type.
helpviewer_keywords: ["StgConvertPropertyToVariant","StgConvertPropertyToVariant function [Structured Storage]","propidl/StgConvertPropertyToVariant","stg.stgconvertpropertytovariant"]
old-location: stg\stgconvertpropertytovariant.htm
tech.root: Stg
ms.assetid: ea4196e6-fc99-4288-942a-e5283f2e5544
ms.date: 12/05/2018
ms.keywords: StgConvertPropertyToVariant, StgConvertPropertyToVariant function [Structured Storage], propidl/StgConvertPropertyToVariant, stg.stgconvertpropertytovariant
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
 - StgConvertPropertyToVariant
 - propidl/StgConvertPropertyToVariant
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
 - StgConvertPropertyToVariant
---

# StgConvertPropertyToVariant function


## -description

The <b>StgConvertPropertyToVariant</b> function converts a <b>SERIALIZEDPROPERTYVALUE</b> data type to a <b>PROPVARIANT</b> data type.

## -parameters

### -param pprop [in]

A pointer to <b>SERIALIZEDPROPERTYVALUE</b>.

### -param CodePage [in]

A property set codepage.

### -param pvar [out]

A pointer to <b>PROPVARIANT</b>.

### -param pma [in]

A pointer to a class that implements the <a href="/windows/desktop/Stg/imemoryallocator">IMemoryAllocator</a> abstract class.

## -returns

Returns <b>TRUE</b> is the property converted was an indirect type (<b>VT_STREAM</b> or <b>VT_STREAMED_OBJECT</b>); otherwise <b>FALSE</b>.

## -remarks

This function converts a property  to a <b>PROPVARIANT</b> data type. If the function fails, it throws an exception that represents an <b>NT_STATUS</b> such as <b>STATUS_INVALID_PARAMETER</b>.

## -see-also

<a href="/windows/desktop/api/propidl/nf-propidl-stgconvertvarianttoproperty">StgConvertVariantToProperty</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant">StgDeserializePropVariant</a>