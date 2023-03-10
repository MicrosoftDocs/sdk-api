---
UID: NS:wtypes.tagCY~r1
title: CY
description: The CY structure is useful for calculations involving money, or for any fixed-point calculation where accuracy is particularly important.
ms.date: 08/03/2022
ms.keywords: tagCY, CY
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
req.typenames: CY
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - tagCY
 - wtypes/tagCY
 - CY
 - wtypes/CY
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wtypes.h
api_name:
 - tagCY
 - CY
---

# CY structure


## -description

A currency number stored as an 8-byte, two's complement integer, scaled by 10,000 to give a fixed-point number with 15 digits to the left of the decimal point and 4 digits to the right. This <b>IDispatch::GetTypeInfo</b> representation provides a range of 922337203685477.5807 to -922337203685477.5808.

The CURRENCY data type is useful for calculations involving money, or for any fixed-point calculation where accuracy is particularly important.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field Lo

### -field Hi

### -field int64

## -remarks

## -see-also

