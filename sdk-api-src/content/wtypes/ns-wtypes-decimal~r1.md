---
UID: NS:wtypes.tagDEC~r1
title: DECIMAL
description: The DECIMAL structure represents a decimal data type that provides a sign and scale for a number.
ms.date: 08/03/2022
ms.keywords: tagDEC, DECIMAL
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: wtypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: DECIMAL
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - tagDEC
 - wtypes/tagDEC
 - DECIMAL
 - wtypes/DECIMAL
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wtypes.h
api_name:
 - tagDEC
 - DECIMAL
---

# DECIMAL structure


## -description

Represents a decimal data type that provides a sign and scale for a number (as in coordinates.)

Decimal variables are stored as 96-bit (12-byte) unsigned integers scaled by a variable power of 10. The power of 10 scaling factor specifies the number of digits to the right of the decimal point, and ranges from 0 to 28.

## -struct-fields

### -field wReserved

Reserved.

### -field DUMMYUNIONNAME

### -field DUMMYSTRUCTNAME

### -field scale

The number of decimal places for the number. Valid values are from 0 to 28. So 12.345 is represented as 12345 with a scale of 3.

### -field sign

Indicates the sign; 0 for positive numbers or DECIMAL_NEG for negative numbers. So -1 is represented as 1 with the DECIMAL_NEG bit set.

### -field signscale

The sign and number of decimal places.

### -field Hi32

The high 32 bits of the number.

### -field DUMMYUNIONNAME2

### -field DUMMYSTRUCTNAME2

### -field Lo32

The low 32 bits of the number.

### -field Mid32

The middle 32 bits of the number.

### -field Lo64

The low 32 bits of the number.

## -remarks

## -see-also

