---
UID: NS:evcoll._EC_VARIANT
title: EC_VARIANT (evcoll.h)
description: Contains event collector data (subscription data) or property values.
helpviewer_keywords: ["*PEC_VARIANT","EC_VARIANT","EC_VARIANT structure","evcoll/EC_VARIANT","wec.ec_variant","wes.ec_variant"]
old-location: wec\ec_variant.htm
tech.root: WEC
ms.assetid: f1f20e33-46b0-458e-ac6c-f890be20c455
ms.date: 12/05/2018
ms.keywords: '*PEC_VARIANT, EC_VARIANT, EC_VARIANT structure, evcoll/EC_VARIANT, wec.ec_variant, wes.ec_variant'
req.header: evcoll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: EC_VARIANT, *PEC_VARIANT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EC_VARIANT
 - evcoll/_EC_VARIANT
 - PEC_VARIANT
 - evcoll/PEC_VARIANT
 - EC_VARIANT
 - evcoll/EC_VARIANT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_VARIANT
---

# EC_VARIANT structure


## -description

The <b>EC_VARIANT</b> structure contains  event collector data (subscription data) or property values.

## -struct-fields

### -field BooleanVal

A Boolean value.

### -field UInt32Val

An unsigned 32-bit integer value.

### -field DateTimeVal

A ULONGLONG value.

### -field StringVal

A null-terminated Unicode string.

### -field BinaryVal

A hexadecimal binary value.

### -field BooleanArr

A pointer to an array of Boolean values.

### -field Int32Arr

A pointer to an array of signed 32-bit integer values.

### -field StringArr

A pointer to an array of null-terminated strings.

### -field PropertyHandleVal

### -field Count

The number of elements (not length) in bytes. Used for arrays and binary or string types.

### -field Type

The type of the data in the structure. Use a value from the <a href="/windows/desktop/api/evcoll/ne-evcoll-ec_variant_type">EC_VARIANT_TYPE</a> enumeration to specify the type. When the type is specified, you can use any of the union members to access the  actual value. For example, if the type is <b>EcVarTypeDateTime</b>, then the value is <b>DateTimeVal</b> in the <b>EC_VARIANT</b> structure.