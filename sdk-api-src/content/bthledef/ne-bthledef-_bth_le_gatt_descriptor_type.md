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

# _BTH_LE_GATT_DESCRIPTOR_TYPE enumeration


## -description


The BTH_LE_GATT_DESCRIPTOR_TYPE enumeration describes the different types of Bluetooth LE generic attributes (GATT).


## -enum-fields




### -field CharacteristicExtendedProperties

The characteristic value has additional properties that describe how it  can be used, or how it can be accessed.


### -field CharacteristicUserDescription

The characteristic value contains a UTF-8 string of variable size that is a user textual
description.


### -field ClientCharacteristicConfiguration

The characteristic value may be configured by the
client.


### -field ServerCharacteristicConfiguration

The characteristic value may be configured for the
server.


### -field CharacteristicFormat

The format of the characteristic value.


### -field CharacteristicAggregateFormat

The format of an aggregated characteristic value.


### -field CustomDescriptor

The characteristic value is customized.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh450843">BTH_LE_GATT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450847">BTH_LE_GATT_DESCRIPTOR_VALUE</a>
 

 

