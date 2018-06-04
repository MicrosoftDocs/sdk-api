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

# __MIDL___MIDL_itf_wcmconfig_0000_0000_0003 enumeration


## -description


Enumerates the data types returned from the <a href="https://msdn.microsoft.com/6ccb99aa-35d5-4f0b-a4f3-a42c4579bc4a">ISettingsItem::GetDataType</a> method. The values correspond appropriately to typical programming types. An exception is the flag value <b>dataTypeFlagArray</b>. This flag may appear combined with <b>dataTypeByte</b> or <b>dataTypeString</b> to indicate xsd:hexBinary or wcm:multiString settings (respectively).

Each of the following constants correspond to a data type.


## -enum-fields




### -field dataTypeByte

Corresponds to a byte.


### -field dataTypeSByte

Corresponds to a signed byte.


### -field dataTypeUInt16

Corresponds to an unsigned 16-bit integer.


### -field dataTypeInt16

Corresponds to a 16-bit integer.


### -field dataTypeUInt32

Corresponds to an unsigned 32-bit integer.


### -field dataTypeInt32

Corresponds to a 32-bit integer.


### -field dataTypeUInt64

Corresponds to an unsigned 64-bit integer.


### -field dataTypeInt64

Corresponds to a 64-bit integer.


### -field dataTypeBoolean

Corresponds to a Boolean.


### -field dataTypeString

Corresponds to a string.


### -field dataTypeFlagArray

This flag may appear combined with <b>dataTypeByte</b> or <b>dataTypeString</b> to indicate xsd:hexBinary or wcm:multiString settings, respectively. 

