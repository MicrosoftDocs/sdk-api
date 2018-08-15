---
UID: NE:evcoll._EC_VARIANT_TYPE
title: "_EC_VARIANT_TYPE"
author: windows-sdk-content
description: The EC_VARIANT_TYPE enumeration defines the values that specify the data types that are used in the Windows Event Collector functions.
old-location: wec\ec_variant_type.htm
old-project: WEC
ms.assetid: 55457e18-e63d-4ebc-be46-d1834b6d62d3
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EC_VARIANT_TYPE, EC_VARIANT_TYPE enumeration, EcVarObjectArrayPropertyHandle, EcVarTypeBoolean, EcVarTypeDateTime, EcVarTypeNull, EcVarTypeString, EcVarTypeUInt32, _EC_VARIANT_TYPE, evcoll/EC_VARIANT_TYPE, evcoll/EcVarObjectArrayPropertyHandle, evcoll/EcVarTypeBoolean, evcoll/EcVarTypeDateTime, evcoll/EcVarTypeNull, evcoll/EcVarTypeString, evcoll/EcVarTypeUInt32, wec.ec_variant_type, wes.ec_variant_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: evcoll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EC_VARIANT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_VARIANT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EC_VARIANT_TYPE enumeration


## -description


The <b>EC_VARIANT_TYPE</b> enumeration defines the values that specify the data types that are used in the Windows Event Collector functions.


## -enum-fields




### -field EcVarTypeNull

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

