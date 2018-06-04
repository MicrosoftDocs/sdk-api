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

# DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS structure


## -description


The <b>DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS</b> structure contains information about a target device.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.friendlyNameFromEdid

A UINT32 value that indicates that the string in the <b>monitorFriendlyDeviceName</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553989">DISPLAYCONFIG_TARGET_DEVICE_NAME</a> structure was constructed from the manufacture identification string in the extended display identification data (EDID).

Setting this member is equivalent to setting the first bit of the 32-bit <b>value</b> member (0x00000001). 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.friendlyNameForced

A UINT32 value that indicates that the target is forced with no detectable monitor attached and the <b>monitorFriendlyDeviceName</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553989">DISPLAYCONFIG_TARGET_DEVICE_NAME</a> structure is a NULL-terminated empty string.

Setting this member is equivalent to setting the second bit of the 32-bit <b>value</b> member (0x00000002). 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.edidIdsValid

A UINT32 value that indicates that the <b>edidManufactureId</b> and <b>edidProductCodeId</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553989">DISPLAYCONFIG_TARGET_DEVICE_NAME</a> structure are valid and were obtained from the EDID.

Setting this member is equivalent to setting the third bit of the 32-bit <b>value</b> member (0x00000004). 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.reserved

This member is reserved and should be set to zero. Setting this member to zero is equivalent to setting the remaining 29 bits (0xFFFFFFF8) of the 32-bit <b>value</b> member to zeros.


### -field DUMMYUNIONNAME.value

A member in the union that DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS contains that can hold a 32-bit value that identifies information about the device.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553989">DISPLAYCONFIG_TARGET_DEVICE_NAME</a>
 

 

