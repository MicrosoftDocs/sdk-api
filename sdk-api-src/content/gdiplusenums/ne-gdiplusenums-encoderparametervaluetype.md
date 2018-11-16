---
UID: NE:gdiplusenums.EncoderParameterValueType
title: EncoderParameterValueType
author: windows-sdk-content
description: The EncoderParameterValueType enumeration specifies data types for image codec (encoder/decoder) parameters. An element of this enumeration is assigned to the Type data member of an EncoderParameter object.
old-location: gdiplus\_gdiplus_ENUM_EncoderParameterValueType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\encoderparametervaluetype.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EncoderParameterValueType, EncoderParameterValueType enumeration [GDI+], EncoderParameterValueTypeASCII, EncoderParameterValueTypeByte, EncoderParameterValueTypeLong, EncoderParameterValueTypeLongRange, EncoderParameterValueTypePointer, EncoderParameterValueTypeRational, EncoderParameterValueTypeRationalRange, EncoderParameterValueTypeShort, EncoderParameterValueTypeUndefined, _gdiplus_ENUM_EncoderParameterValueType, gdiplus._gdiplus_ENUM_EncoderParameterValueType, gdiplusenums/EncoderParameterValueType, gdiplusenums/EncoderParameterValueTypeASCII, gdiplusenums/EncoderParameterValueTypeByte, gdiplusenums/EncoderParameterValueTypeLong, gdiplusenums/EncoderParameterValueTypeLongRange, gdiplusenums/EncoderParameterValueTypePointer, gdiplusenums/EncoderParameterValueTypeRational, gdiplusenums/EncoderParameterValueTypeRationalRange, gdiplusenums/EncoderParameterValueTypeShort, gdiplusenums/EncoderParameterValueTypeUndefined
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - EncoderParameterValueType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# EncoderParameterValueType enumeration


## -description


The <b>EncoderParameterValueType</b> enumeration specifies data types for image codec (encoder/decoder) parameters. An element of this enumeration is assigned to the 
			<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">Type</a> data member of an <b>EncoderParameter</b> object. 


## -enum-fields




### -field EncoderParameterValueTypeByte

Specifies that the parameter is an 8-bit unsigned integer. 


### -field EncoderParameterValueTypeASCII

Specifies that the parameter is a null-terminated character string. 


### -field EncoderParameterValueTypeShort

Specifies that the parameter is a 16-bit unsigned integer. 


### -field EncoderParameterValueTypeLong

Specifies that the parameter is a 32-bit unsigned integer. 


### -field EncoderParameterValueTypeRational

Specifies that the parameter is an array of two, 32-bit unsigned integers. The pair of integers represents a fraction. The first integer in the pair is the numerator, and the second integer in the pair is the denominator. 


### -field EncoderParameterValueTypeLongRange

Specifies that the parameter is an array of two, 32-bit unsigned integers. The pair of integers represents a range of numbers. The first integer is the smallest number in the range, and the second integer is the largest number in the range. 


### -field EncoderParameterValueTypeUndefined

Specifies that the parameter is an array of bytes that can hold values of any type. 


### -field EncoderParameterValueTypeRationalRange

Specifies that the parameter is an array of four, 32-bit unsigned integers. The first two integers represent one fraction, and the second two integers represent a second fraction. The two fractions represent a range of rational numbers. The first fraction is the smallest rational number in the range, and the second fraction is the largest rational number in the range. 


### -field EncoderParameterValueTypePointer

Specifies that the parameter is a pointer to a block of custom metadata.


## -see-also




<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a>
 

 

