---
UID: NE:gdiplusenums.EncoderParameterValueType
title: EncoderParameterValueType (gdiplusenums.h)
description: The EncoderParameterValueType enumeration specifies data types for image codec (encoder/decoder) parameters. An element of this enumeration is assigned to the Type data member of an EncoderParameter object.
helpviewer_keywords: ["EncoderParameterValueType","EncoderParameterValueType enumeration [GDI+]","EncoderParameterValueTypeASCII","EncoderParameterValueTypeByte","EncoderParameterValueTypeLong","EncoderParameterValueTypeLongRange","EncoderParameterValueTypePointer","EncoderParameterValueTypeRational","EncoderParameterValueTypeRationalRange","EncoderParameterValueTypeShort","EncoderParameterValueTypeUndefined","_gdiplus_ENUM_EncoderParameterValueType","gdiplus._gdiplus_ENUM_EncoderParameterValueType","gdiplusenums/EncoderParameterValueType","gdiplusenums/EncoderParameterValueTypeASCII","gdiplusenums/EncoderParameterValueTypeByte","gdiplusenums/EncoderParameterValueTypeLong","gdiplusenums/EncoderParameterValueTypeLongRange","gdiplusenums/EncoderParameterValueTypePointer","gdiplusenums/EncoderParameterValueTypeRational","gdiplusenums/EncoderParameterValueTypeRationalRange","gdiplusenums/EncoderParameterValueTypeShort","gdiplusenums/EncoderParameterValueTypeUndefined"]
old-location: gdiplus\_gdiplus_ENUM_EncoderParameterValueType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\encoderparametervaluetype.htm
ms.date: 12/05/2018
ms.keywords: EncoderParameterValueType, EncoderParameterValueType enumeration [GDI+], EncoderParameterValueTypeASCII, EncoderParameterValueTypeByte, EncoderParameterValueTypeLong, EncoderParameterValueTypeLongRange, EncoderParameterValueTypePointer, EncoderParameterValueTypeRational, EncoderParameterValueTypeRationalRange, EncoderParameterValueTypeShort, EncoderParameterValueTypeUndefined, _gdiplus_ENUM_EncoderParameterValueType, gdiplus._gdiplus_ENUM_EncoderParameterValueType, gdiplusenums/EncoderParameterValueType, gdiplusenums/EncoderParameterValueTypeASCII, gdiplusenums/EncoderParameterValueTypeByte, gdiplusenums/EncoderParameterValueTypeLong, gdiplusenums/EncoderParameterValueTypeLongRange, gdiplusenums/EncoderParameterValueTypePointer, gdiplusenums/EncoderParameterValueTypeRational, gdiplusenums/EncoderParameterValueTypeRationalRange, gdiplusenums/EncoderParameterValueTypeShort, gdiplusenums/EncoderParameterValueTypeUndefined
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - EncoderParameterValueType
 - gdiplusenums/EncoderParameterValueType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - EncoderParameterValueType
---

# EncoderParameterValueType enumeration


## -description

The <b>EncoderParameterValueType</b> enumeration specifies data types for image codec (encoder/decoder) parameters. An element of this enumeration is assigned to the 
			<a href="/previous-versions/ms534434(v=vs.85)">Type</a> data member of an <b>EncoderParameter</b> object.

## -enum-fields

### -field EncoderParameterValueTypeByte:1

Specifies that the parameter is an 8-bit unsigned integer.

### -field EncoderParameterValueTypeASCII:2

Specifies that the parameter is a null-terminated character string.

### -field EncoderParameterValueTypeShort:3

Specifies that the parameter is a 16-bit unsigned integer.

### -field EncoderParameterValueTypeLong:4

Specifies that the parameter is a 32-bit unsigned integer.

### -field EncoderParameterValueTypeRational:5

Specifies that the parameter is an array of two, 32-bit unsigned integers. The pair of integers represents a fraction. The first integer in the pair is the numerator, and the second integer in the pair is the denominator.

### -field EncoderParameterValueTypeLongRange:6

Specifies that the parameter is an array of two, 32-bit unsigned integers. The pair of integers represents a range of numbers. The first integer is the smallest number in the range, and the second integer is the largest number in the range.

### -field EncoderParameterValueTypeUndefined:7

Specifies that the parameter is an array of bytes that can hold values of any type.

### -field EncoderParameterValueTypeRationalRange:8

Specifies that the parameter is an array of four, 32-bit unsigned integers. The first two integers represent one fraction, and the second two integers represent a second fraction. The two fractions represent a range of rational numbers. The first fraction is the smallest rational number in the range, and the second fraction is the largest rational number in the range.

### -field EncoderParameterValueTypePointer:9     

Specifies that the parameter is a pointer to a block of custom metadata.

## -see-also

<a href="/previous-versions/ms534434(v=vs.85)">EncoderParameter</a>
