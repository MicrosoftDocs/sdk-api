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

# _EC_VARIANT structure


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

The type of the data in the structure. Use a value from the <a href="https://msdn.microsoft.com/55457e18-e63d-4ebc-be46-d1834b6d62d3">EC_VARIANT_TYPE</a> enumeration to specify the type. When the type is specified, you can use any of the union members to access the  actual value. For example, if the type is <b>EcVarTypeDateTime</b>, then the value is <b>DateTimeVal</b> in the <b>EC_VARIANT</b> structure.

