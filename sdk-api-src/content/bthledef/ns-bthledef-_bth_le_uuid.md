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

# _BTH_LE_UUID structure


## -description


The BTH_LE_UUID structure contains information about a Bluetooth Low Energy (LE) Universally Unique Identifier (UUID).


## -struct-fields




### -field IsShortUuid

Indicates if the Low Energy (LE) UUID a 16-bit shortened value, or if it is the long 128-bit value.


### -field Value

 


### -field Value.ShortUuid

 


### -field Value.ShortUuid.case

 


### -field Value.ShortUuid.case.TRUE

 


### -field Value.LongUuid

 


### -field Value.LongUuid.case

 


### -field Value.LongUuid.case.FALSE

 


### -field Value.switch_type

 


### -field Value.switch_type.BOOLEAN

 


### -field Value.switch_is

 


### -field Value.switch_is.(BOOLEAN)IsShortUuid

 




#### - LongUuid

The long 128-bit value of the UUID. This member applies only if <b>IsShortUuid</b> is FALSE.


#### - ShortUuid

The short 16-bit value of the UUID. This member applies only if <b>IsShortUuid</b> is TRUE.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh450850">BTH_LE_GATT_SERVICE</a>
 

 

