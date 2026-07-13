---
UID: NS:oaidl.tagVARIANT
title: VARIANT (oaidl.h)
description: VARIANTARG describes arguments passed within DISPPARAMS, and VARIANT to specify variant data that cannot be passed by reference.
helpviewer_keywords: ["*LPVARIANT","*LPVARIANTARG","LPVARIANT","LPVARIANT structure pointer [Automation]","LPVARIANTARG","LPVARIANTARG structure pointer [Automation]","VARIANT","VARIANT structure [Automation]","VARIANTARG","VARIANTARG structure [Automation]","_oa96_VARIANT_and_VARIANTARG","automat.variant","oaidl/LPVARIANT","oaidl/LPVARIANTARG","oaidl/VARIANT","oaidl/VARIANTARG"]
old-location: automat\variant.htm
tech.root: automat
ms.assetid: e305240e-9e11-4006-98cc-26f4932d2118
ms.date: 12/05/2018
ms.keywords: '*LPVARIANT, *LPVARIANTARG, LPVARIANT, LPVARIANT structure pointer [Automation], LPVARIANTARG, LPVARIANTARG structure pointer [Automation], VARIANT, VARIANT structure [Automation], VARIANTARG, VARIANTARG structure [Automation], _oa96_VARIANT_and_VARIANTARG, automat.variant, oaidl/LPVARIANT, oaidl/LPVARIANTARG, oaidl/VARIANT, oaidl/VARIANTARG'
req.header: oaidl.h
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
req.typenames: VARIANT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVARIANT
 - oaidl/tagVARIANT
 - VARIANT
 - oaidl/VARIANT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - VARIANT
---

# VARIANT structure


## -description

<b>VARIANTARG</b> describes arguments passed within DISPPARAMS, and <b>VARIANT</b> to specify variant data that cannot be passed by reference.

When a variant refers to another variant by using the VT_VARIANT | VT_BYREF vartype, the variant being referred to cannot also be of type VT_VARIANT | VT_BYREF. VARIANTs can be passed by value, even if VARIANTARGs cannot.

## -struct-fields

### -field __VARIANT_NAME_1

### -field __VARIANT_NAME_1.__VARIANT_NAME_2

Type: <b>struct __tagVARIANT</b>


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.vt

Type: <b>VARTYPE</b>

The type of data in the union.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.wReserved1

Type: <b>WORD</b>

Reserved.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.wReserved2

Type: <b>WORD</b>

Reserved.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.wReserved3

Type: <b>WORD</b>

Reserved.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3

###### __VARIANT_NAME_2.__VARIANT_NAME_3.bool

Type: <b>_VARIANT_BOOL</b>

A 16-bit Boolean value. A value of 0xFFFF (all bits 1) indicates true; a value of 0 (all bits 0) indicates false. No other values are valid.




###### __VARIANT_NAME_2.__VARIANT_NAME_3.pbool

Type: <b>_VARIANT_BOOL*</b>

A reference to a 16-bit Boolean value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.llVal

Type: <b>LONGLONG</b>

An 8-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.lVal

Type: <b>LONG</b>

A 4-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.bVal

Type: <b>BYTE</b>

An unsigned 1-byte character.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.iVal

Type: <b>SHORT</b>

A 2-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.fltVal

Type: <b>FLOAT</b>

A 4-byte real value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.dblVal

Type: <b>DOUBLE</b>

An 8-byte real value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.boolVal

Type: <b>VARIANT_BOOL</b>

A 16-bit Boolean value. A value of 0xFFFF (all bits 1) indicates true; a value of 0 (all bits 0) indicates false. No other values are valid.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.scode

Type: <b>SCODE</b>

An SCODE value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.cyVal

Type: <b>CY</b>

A currency value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.date

Type: <b>DATE</b>

A date and time value. Dates are represented as double-precision numbers, where midnight, January 1, 1900 is 2.0, January 2, 1900 is 3.0, and so on.

The date can be converted to and from an MS-DOS representation using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-varianttimetodosdatetime">VariantTimeToDosDateTime</a>.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.bstrVal

Type: <b>BSTR</b>

A string value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.punkVal

Type: <b>IUnknown*</b>

A pointer to an object that implements the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pdispVal

Type: <b>IDispatch*</b>

A pointer to an object was specified.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.parray

Type: <b>SAFEARRAY*</b>

A safe array descriptor, which describes the dimensions, size, and in-memory location of the array.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pbVal

Type: <b>BYTE*</b>

A reference to an unsigned 1-byte character.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.piVal

Type: <b>SHORT*</b>

A reference to a 2-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.plVal

Type: <b>LONG*</b>

A reference to a 4-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pllVal

Type: <b>LONGLONG*</b>

A reference to an 8-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pfltVal

Type: <b>FLOAT*</b>

A reference to a 4-byte real value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pdblVal

Type: <b>DOUBLE*</b>

A reference to an 8-byte real value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pboolVal

Type: <b>VARIANT_BOOL*</b>

A reference to a 16-bit Boolean value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pscode

Type: <b>SCODE*</b>

A reference to an SCODE value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pcyVal

Type: <b>CY*</b>

A reference to a currency value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pdate

Type: <b>DATE*</b>

A reference to a date and time value. Dates are represented as double-precision numbers, where midnight, January 1, 1900 is 2.0, January 2, 1900 is 3.0, and so on.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pbstrVal

Type: <b>BSTR*</b>

A reference to a string value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.ppunkVal

Type: <b>IUnknown**</b>

A reference to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.ppdispVal

Type: <b>IDispatch**</b>

A reference to an object pointer.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pparray

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pvarVal

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.byref

Type: <b>PVOID</b>

A generic value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.cVal

Type: <b>CHAR</b>

A 1-byte character value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.uiVal

Type: <b>USHORT</b>

An unsigned 2-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.ulVal

Type: <b>ULONG</b>

An unsigned 4-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.ullVal

Type: <b>ULONGLONG</b>

An unsigned 8-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.intVal

Type: <b>INT</b>

An integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.uintVal

Type: <b>UINT</b>

An unsigned integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pdecVal

Type: <b>DECIMAL*</b>

A decimal value, which is stored as 96-bit (12-byte) unsigned integers scaled by a variable power of 10.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pcVal

Type: <b>CHAR*</b>

A reference to a 1-byte character value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.puiVal

Type: <b>USHORT*</b>

A reference to an unsigned 2-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pulVal

Type: <b>ULONG*</b>

A reference to an unsigned 4-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pullVal

Type: <b>ULONGLONG*</b>

A reference to an unsigned 8-byte integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pintVal

Type: <b>INT*</b>

A reference to an integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.puintVal

Type: <b>UINT*</b>

A reference to an unsigned integer value.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.__VARIANT_NAME_4

Type: <b>struct __tagBRECORD</b>


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.__VARIANT_NAME_4.pvRecord

Type: <b>PVOID</b>

A reference to a database record.

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.__VARIANT_NAME_4.pRecInfo

Type: <b><a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>*</b>

A reference to a UDT.

### -field __VARIANT_NAME_1.decVal

Type: <b>DECIMAL</b>

A decimal value.