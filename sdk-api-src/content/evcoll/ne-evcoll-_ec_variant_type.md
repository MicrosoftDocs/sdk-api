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

