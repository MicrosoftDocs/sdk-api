---
UID: NS:evcoll._EC_VARIANT
title: "_EC_VARIANT"
author: windows-sdk-content
description: Contains event collector data (subscription data) or property values.
old-location: wec\ec_variant.htm
old-project: WEC
ms.assetid: f1f20e33-46b0-458e-ac6c-f890be20c455
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PEC_VARIANT, EC_VARIANT, EC_VARIANT structure, _EC_VARIANT, evcoll/EC_VARIANT, wec.ec_variant, wes.ec_variant"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: EC_VARIANT, *PEC_VARIANT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_VARIANT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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

