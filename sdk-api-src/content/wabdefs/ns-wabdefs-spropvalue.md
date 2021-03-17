---
UID: NS:wabdefs._SPropValue
title: SPropValue (wabdefs.h)
description: Do not use. Contains the property tag values.
helpviewer_keywords: ["*LPSPropValue","SPropValue","SPropValue structure [Windows Address Book]","_wab_SPropValue","wab._wab_SPropValue","wabdefs/SPropValue"]
old-location: wab\_wab_SPropValue.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\spropvalue.htm
ms.date: 12/05/2018
ms.keywords: '*LPSPropValue, SPropValue, SPropValue structure [Windows Address Book], _wab_SPropValue, wab._wab_SPropValue, wabdefs/SPropValue'
req.header: wabdefs.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SPropValue, *LPSPropValue
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _SPropValue
 - wabdefs/_SPropValue
 - LPSPropValue
 - wabdefs/LPSPropValue
 - SPropValue
 - wabdefs/SPropValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - SPropValue
---

# SPropValue structure


## -description

Do not use. Contains the property tag values.

## -struct-fields

### -field ulPropTag

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the property tag for the property. Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.

### -field dwAlignPad

Type: <b>ULONG</b>

### -field Value

Union of data values, with the specific value dictated by the property type. The following text provides a list for each property type of the member of the union to be used and its associated data type.



#### i

<b>Type: <b>short</b>
</b>
PT_I2 or PT_SHORT



#### l

<b>Type: <b>LONG</b>
</b>
PT_LONG



#### ul

<b>Type: <b>ULONG</b>
</b>
PT_LONG



#### flt

<b>Type: <b>float</b>
</b>
PT_R4



#### dbl

<b>Type: <b>double</b>
</b>
PT_DOUBLE



#### b

<b>Type: <b>USHORT</b>
</b>
PT_BOOLEAN



#### cur

<b>Type: <b>CURRENCY</b>
</b>
PT_CURRENCY



#### at

<b>Type: <b>double</b>
</b>
PT_APPTIME



#### ft

<b>Type: <b>FILETIME</b>
</b>
PT_SYSTIME



#### lpszA

<b>Type: <b>LPSTR</b>
</b>
PT_STRING8



#### bin

<b>Type: <b><a href="/previous-versions/office/developer/office-2007/cc815817(v=office.12)">SBinary</a></b>
</b>
PT_BINARY



#### lpszW

<b>Type: <b>LPWSTR</b>
</b>
PT_UNICODE



#### lpguid

<b>Type: <b>LPGUID</b>
</b>
PT_CLSID



#### li

<b>Type: <b>LARGE_INTEGER</b>
</b>
PT_I8



#### MVi

<b>Type: <b>SShortArray</b>
</b>
PT_MV_I2



#### MVl

<b>Type: <b>SLongArray</b>
</b>
PT_MV_LONG



#### MVflt

<b>Type: <b>SRealArray</b>
</b>
PT_MV_R4



#### MVdbl

<b>Type: <b>SDoubleArray</b>
</b>
PT_MV_DOUBLE



#### MVcur

<b>Type: <b>SCurrencyArray</b>
</b>
PT_MV_CURRENCY



#### MVat

<b>Type: <b>SAppTimeArray</b>
</b>
PT_MV_APPTIME



#### MVft

<b>Type: <b>SDateTimeArray</b>
</b>
PT_MV_SYSTIME



#### MVbin

<b>Type: <b><a href="/previous-versions/office/developer/office-2007/cc815398(v=office.12)">SBinaryArray</a></b>
</b>
PT_MV_BINARY



#### MVszA

<b>Type: <b>SLPSTRArray</b>
</b>
PT_MV_STRING8



#### MVszW

<b>Type: <b>SWStringArray</b>
</b>
PT_MV_UNICODE



#### MVguid

<b>Type: <b>SGuidArray</b>
</b>
PT_MV_CLSID



#### MVli

<b>Type: <b>SLargeIntegerArray</b>
</b>
PT_MV_I8



#### err

<b>Type: <b>SCODE</b>
</b>
PT_ERROR



#### x

<b>Type: <b>LONG</b>
</b>
PT_NULL, PT_OBJECT (no usable value)

### -field _PV