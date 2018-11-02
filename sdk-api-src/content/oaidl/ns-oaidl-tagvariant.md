---
UID: NS:oaidl.tagVARIANT
title: tagVARIANT
author: windows-sdk-content
description: VARIANTARG describes arguments passed within DISPPARAMS, and VARIANT to specify variant data that cannot be passed by reference.
old-location: automat\variant.htm
tech.root: automat
ms.assetid: e305240e-9e11-4006-98cc-26f4932d2118
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPVARIANT, *LPVARIANTARG, LPVARIANT, LPVARIANT structure pointer [Automation], LPVARIANTARG, LPVARIANTARG structure pointer [Automation], VARIANT, VARIANT structure [Automation], VARIANTARG, VARIANTARG structure [Automation], _oa96_VARIANT_and_VARIANTARG, automat.variant, oaidl/LPVARIANT, oaidl/LPVARIANTARG, oaidl/VARIANT, oaidl/VARIANTARG, tagVARIANT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - VARIANT
product: Windows
targetos: Windows
req.typenames: VARIANT
req.redist: 
---

# tagVARIANT structure


## -description


<b>VARIANTARG</b> describes arguments passed within DISPPARAMS, and <b>VARIANT</b> to specify variant data that cannot be passed by reference.

When a variant refers to another variant by using the VT_VARIANT | VT_BYREF vartype, the variant being referred to cannot also be of type VT_VARIANT | VT_BYREF. VARIANTs can be passed by value, even if VARIANTARGs cannot.


## -struct-fields




### -field __VARIANT_NAME_1


### -field __VARIANT_NAME_1.__VARIANT_NAME_2

<b>Type: <b>struct __tagVARIANT</b>
</b>

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.vt

<b>Type: <b>VARTYPE</b>
</b>
The type of data in the union.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.wReserved1

<b>Type: <b>WORD</b>
</b>
Reserved.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.wReserved2

<b>Type: <b>WORD</b>
</b>
Reserved.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.wReserved3

<b>Type: <b>WORD</b>
</b>
Reserved.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3



###### __VARIANT_NAME_2.__VARIANT_NAME_3.bool

<b>Type: <b>_VARIANT_BOOL</b>
</b>
A 16-bit Boolean value. A value of 0xFFFF (all bits 1) indicates true; a value of 0 (all bits 0) indicates false. No other values are valid.




###### __VARIANT_NAME_2.__VARIANT_NAME_3.pbool

<b>Type: <b>_VARIANT_BOOL*</b>
</b>
A reference to a 16-bit Boolean value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.llVal

<b>Type: <b>LONGLONG</b>
</b>
An 8-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.lVal

<b>Type: <b>LONG</b>
</b>
A 4-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.bVal

<b>Type: <b>BYTE</b>
</b>
An unsigned 1-byte character.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.iVal

<b>Type: <b>SHORT</b>
</b>
A 2-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.fltVal

<b>Type: <b>FLOAT</b>
</b>
A 4-byte real value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.dblVal

<b>Type: <b>DOUBLE</b>
</b>
An 8-byte real value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.boolVal

<b>Type: <b>VARIANT_BOOL</b>
</b>
A 16-bit Boolean value. A value of 0xFFFF (all bits 1) indicates true; a value of 0 (all bits 0) indicates false. No other values are valid.



### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.scode

<b>Type: <b>SCODE</b>
</b>
An SCODE value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.cyVal

<b>Type: <b>CY</b>
</b>
A currency value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.date

<b>Type: <b>DATE</b>
</b>
A date and time value. Dates are represented as double-precision numbers, where midnight, January 1, 1900 is 2.0, January 2, 1900 is 3.0, and so on.

The date can be converted to and from an MS-DOS representation using <a href="https://msdn.microsoft.com/62307266-2434-4b06-9135-8854f4624c5c">VariantTimeToDosDateTime</a>.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.bstrVal

<b>Type: <b>BSTR</b>
</b>
A string value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.punkVal

<b>Type: <b>IUnknown*</b>
</b>
A pointer to an object that implements the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pdispVal

<b>Type: <b>IDispatch*</b>
</b>
A pointer to an object was specified.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.parray

<b>Type: <b>SAFEARRAY*</b>
</b>
A safe array descriptor, which describes the dimensions, size, and in-memory location of the array.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pbVal

<b>Type: <b>BYTE*</b>
</b>
A reference to an unsigned 1-byte character.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.piVal

<b>Type: <b>SHORT*</b>
</b>
A reference to a 2-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.plVal

<b>Type: <b>LONG*</b>
</b>
A reference to a 4-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pllVal

<b>Type: <b>LONGLONG*</b>
</b>
A reference to an 8-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pfltVal

<b>Type: <b>FLOAT*</b>
</b>
A reference to a 4-byte real value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pdblVal

<b>Type: <b>DOUBLE*</b>
</b>
A reference to an 8-byte real value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pboolVal

<b>Type: <b>VARIANT_BOOL*</b>
</b>
A reference to a 16-bit Boolean value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pscode

<b>Type: <b>SCODE*</b>
</b>
A reference to an SCODE value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pcyVal

<b>Type: <b>CY*</b>
</b>
A reference to a currency value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pdate

<b>Type: <b>DATE*</b>
</b>
A reference to a date and time value. Dates are represented as double-precision numbers, where midnight, January 1, 1900 is 2.0, January 2, 1900 is 3.0, and so on.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pbstrVal

<b>Type: <b>BSTR*</b>
</b>
A reference to a string value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.ppunkVal

<b>Type: <b>IUnknown**</b>
</b>
A reference to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointer.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.ppdispVal

<b>Type: <b>IDispatch**</b>
</b>
A reference to an object pointer.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pparray

 


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pvarVal

 


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.byref

<b>Type: <b>PVOID</b>
</b>
A generic value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.cVal

<b>Type: <b>CHAR</b>
</b>
A 1-byte character value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.uiVal

<b>Type: <b>USHORT</b>
</b>
An unsigned 2-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.ulVal

<b>Type: <b>ULONG</b>
</b>
An unsigned 4-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.ullVal

<b>Type: <b>ULONGLONG</b>
</b>
An unsigned 8-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.intVal

<b>Type: <b>INT</b>
</b>
An integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.uintVal

<b>Type: <b>UINT</b>
</b>
An unsigned integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pdecVal

<b>Type: <b>DECIMAL*</b>
</b>
A decimal value, which is stored as 96-bit (12-byte) unsigned integers scaled by a variable power of 10.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pcVal

<b>Type: <b>CHAR*</b>
</b>
A reference to a 1-byte character value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.puiVal

<b>Type: <b>USHORT*</b>
</b>
A reference to an unsigned 2-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pulVal

<b>Type: <b>ULONG*</b>
</b>
A reference to an unsigned 4-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pullVal

<b>Type: <b>ULONGLONG*</b>
</b>
A reference to an unsigned 8-byte integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.pintVal

<b>Type: <b>INT*</b>
</b>
A reference to an integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.puintVal

<b>Type: <b>UINT*</b>
</b>
A reference to an unsigned integer value.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.__VARIANT_NAME_4

<b>Type: <b>struct __tagBRECORD</b>
</b>

### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.__VARIANT_NAME_4.pvRecord

<b>Type: <b>PVOID</b>
</b>
A reference to a database record.


### -field __VARIANT_NAME_1.__VARIANT_NAME_2.__VARIANT_NAME_3.__VARIANT_NAME_4.pRecInfo

<b>Type: <b><a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>*</b>
</b>
A reference to a UDT.


### -field __VARIANT_NAME_1.decVal

<b>Type: <b>DECIMAL</b>
</b>
A decimal value.

