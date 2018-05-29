---
UID: NS:wingdi.DISPLAYCONFIG_SET_TARGET_PERSISTENCE
title: DISPLAYCONFIG_SET_TARGET_PERSISTENCE
author: windows-sdk-content
description: The DISPLAYCONFIG_SET_TARGET_PERSISTENCE structure contains information about setting the display.
old-location: display\displayconfig_set_target_persistence.htm
old-project: display
ms.assetid: 4798a1e1-8685-40c2-917a-0ee071bc780c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CCD_Structures_705e98bf-b3ea-4d2b-8c93-ffb300d700c8.xml, DISPLAYCONFIG_SET_TARGET_PERSISTENCE, DISPLAYCONFIG_SET_TARGET_PERSISTENCE structure [Display Devices], display.displayconfig_set_target_persistence, wingdi/DISPLAYCONFIG_SET_TARGET_PERSISTENCE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
req.typenames: DISPLAYCONFIG_SET_TARGET_PERSISTENCE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wingdi.h
api_name:
-	DISPLAYCONFIG_SET_TARGET_PERSISTENCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DISPLAYCONFIG_SET_TARGET_PERSISTENCE structure


## -description


The DISPLAYCONFIG_SET_TARGET_PERSISTENCE structure contains information about setting the display.


## -struct-fields




### -field header

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains information for setting the target persistence. The <b>type</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER is set to DISPLAYCONFIG_DEVICE_INFO_SET_TARGET_PERSISTENCE. DISPLAYCONFIG_DEVICE_INFO_HEADER also contains the adapter and target identifiers of the target to set the persistence for. The <b>size</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER is set to at least the size of the DISPLAYCONFIG_SET_TARGET_PERSISTENCE structure.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.bootPersistenceOn

A UINT32 value that specifies whether the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a> function should enable or disable boot persistence for the specified target. 

Setting this member is equivalent to setting the first bit of the 32-bit <b>value</b> member (0x00000001). 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.reserved

This member is reserved and should be set to zero. Setting this member to zero is equivalent to setting the remaining 31 bits (0xFFFFFFFE) of the 32-bit <b>value</b> member to zeros. 


### -field DUMMYUNIONNAME.value

A member in the union that DISPLAYCONFIG_SET_TARGET_PERSISTENCE contains that can hold a 32-bit value that identifies information about setting the display. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a>
 

 

