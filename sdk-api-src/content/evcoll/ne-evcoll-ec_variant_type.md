---
UID: NE:evcoll._EC_VARIANT_TYPE
title: EC_VARIANT_TYPE (evcoll.h)
description: The EC_VARIANT_TYPE enumeration defines the values that specify the data types that are used in the Windows Event Collector functions.
helpviewer_keywords: ["EC_VARIANT_TYPE","EC_VARIANT_TYPE enumeration","EcVarObjectArrayPropertyHandle","EcVarTypeBoolean","EcVarTypeDateTime","EcVarTypeNull","EcVarTypeString","EcVarTypeUInt32","evcoll/EC_VARIANT_TYPE","evcoll/EcVarObjectArrayPropertyHandle","evcoll/EcVarTypeBoolean","evcoll/EcVarTypeDateTime","evcoll/EcVarTypeNull","evcoll/EcVarTypeString","evcoll/EcVarTypeUInt32","wec.ec_variant_type","wes.ec_variant_type"]
old-location: wec\ec_variant_type.htm
tech.root: WEC
ms.assetid: 55457e18-e63d-4ebc-be46-d1834b6d62d3
ms.date: 12/05/2018
ms.keywords: EC_VARIANT_TYPE, EC_VARIANT_TYPE enumeration, EcVarObjectArrayPropertyHandle, EcVarTypeBoolean, EcVarTypeDateTime, EcVarTypeNull, EcVarTypeString, EcVarTypeUInt32, evcoll/EC_VARIANT_TYPE, evcoll/EcVarObjectArrayPropertyHandle, evcoll/EcVarTypeBoolean, evcoll/EcVarTypeDateTime, evcoll/EcVarTypeNull, evcoll/EcVarTypeString, evcoll/EcVarTypeUInt32, wec.ec_variant_type, wes.ec_variant_type
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
req.typenames: EC_VARIANT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EC_VARIANT_TYPE
 - evcoll/_EC_VARIANT_TYPE
 - EC_VARIANT_TYPE
 - evcoll/EC_VARIANT_TYPE
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
 - EC_VARIANT_TYPE
---

# EC_VARIANT_TYPE enumeration


## -description

The <b>EC_VARIANT_TYPE</b> enumeration defines the values that specify the data types that are used in the Windows Event Collector functions.

## -enum-fields

### -field EcVarTypeNull:0

Null content that implies that the element that contains the content does not exist.

### -field EcVarTypeBoolean

A Boolean value.

### -field EcVarTypeUInt32

An unsigned 32-bit value.

### -field EcVarTypeDateTime

A ULONGLONG value.

### -field EcVarTypeString

A string value.

### -field EcVarObjectArrayPropertyHandle

An EC_OBJECT_ARRAY_PROPERTY_HANDLE value.

