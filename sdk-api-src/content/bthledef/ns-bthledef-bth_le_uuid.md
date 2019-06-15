---
UID: NS:bthledef._BTH_LE_UUID
title: BTH_LE_UUID (bthledef.h)
author: windows-sdk-content
description: The BTH_LE_UUID structure contains information about a Bluetooth Low Energy (LE) Universally Unique Identifier (UUID).
old-location: bltooth\bth_le_uuid.htm
tech.root: bltooth
ms.assetid: FA82A099-7924-44A1-A14C-7633B8656FB7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PBTH_LE_UUID, BTH_LE_UUID, BTH_LE_UUID structure [Bluetooth Devices], PBTH_LE_UUID, PBTH_LE_UUID structure pointer [Bluetooth Devices], bltooth.bth_le_uuid, bthledef/BTH_LE_UUID, bthledef/PBTH_LE_UUID"
ms.topic: struct
req.header: bthledef.h
req.include-header: BthLEDef.h
req.target-type: Windows
req.target-min-winverclnt: Versions:\_Supported in Windows 8
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - BthLEDef.h
api_name:
 - BTH_LE_UUID
product: Windows
targetos: Windows
req.typenames: BTH_LE_UUID, *PBTH_LE_UUID
req.redist: 
ms.custom: 19H1
---

# BTH_LE_UUID structure


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




<a href="https://docs.microsoft.com/windows/desktop/api/bthledef/ns-bthledef-_bth_le_gatt_service">BTH_LE_GATT_SERVICE</a>
 

 

