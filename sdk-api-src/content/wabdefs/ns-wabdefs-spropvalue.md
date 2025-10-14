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

Type: <b>short</b>

PT_I2 or PT_SHORT



#### l

Type: <b>LONG</b>

PT_LONG



#### ul

Type: <b>ULONG</b>

PT_LONG



#### flt

Type: <b>float</b>

PT_R4



#### dbl

Type: <b>double</b>

PT_DOUBLE



#### b

Type: <b>USHORT</b>

PT_BOOLEAN



#### cur

Type: <b>CURRENCY</b>

PT_CURRENCY



#### at

Type: <b>double</b>

PT_APPTIME



#### ft

Type: <b>FILETIME</b>

PT_SYSTIME



#### lpszA

Type: <b>LPSTR</b>

PT_STRING8



#### bin

Type: <b><a href="/previous-versions/office/developer/office-2007/cc815817(v=office.12)">SBinary</a></b>

PT_BINARY



#### lpszW

Type: <b>LPWSTR</b>

PT_UNICODE



#### lpguid

Type: <b>LPGUID</b>

PT_CLSID



#### li

Type: <b>LARGE_INTEGER</b>

PT_I8



#### MVi

Type: <b>SShortArray</b>

PT_MV_I2



#### MVl

Type: <b>SLongArray</b>

PT_MV_LONG



#### MVflt

Type: <b>SRealArray</b>

PT_MV_R4



#### MVdbl

Type: <b>SDoubleArray</b>

PT_MV_DOUBLE



#### MVcur

Type: <b>SCurrencyArray</b>

PT_MV_CURRENCY



#### MVat

Type: <b>SAppTimeArray</b>

PT_MV_APPTIME



#### MVft

Type: <b>SDateTimeArray</b>

PT_MV_SYSTIME



#### MVbin

Type: <b><a href="/previous-versions/office/developer/office-2007/cc815398(v=office.12)">SBinaryArray</a></b>

PT_MV_BINARY



#### MVszA

Type: <b>SLPSTRArray</b>

PT_MV_STRING8



#### MVszW

Type: <b>SWStringArray</b>

PT_MV_UNICODE



#### MVguid

Type: <b>SGuidArray</b>

PT_MV_CLSID



#### MVli

Type: <b>SLargeIntegerArray</b>

PT_MV_I8



#### err

Type: <b>SCODE</b>

PT_ERROR



#### x

Type: <b>LONG</b>

PT_NULL, PT_OBJECT (no usable value)

### -field _PV