---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# EncoderParameterValueType enumeration


## -description


The <b>EncoderParameterValueType</b> enumeration specifies data types for image codec (encoder/decoder) parameters. An element of this enumeration is assigned to the 
			<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> data member of an <b>EncoderParameter</b> object. 


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
 

 

