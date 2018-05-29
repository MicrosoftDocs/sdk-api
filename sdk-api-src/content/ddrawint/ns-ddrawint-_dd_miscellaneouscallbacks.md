---
UID: NS:ddrawint._DD_MISCELLANEOUSCALLBACKS
title: "_DD_MISCELLANEOUSCALLBACKS"
author: windows-sdk-content
description: The DD_MISCELLANEOUSCALLBACKS structure contains an entry pointer to the memory query callback that a device driver supports.
old-location: display\dd_miscellaneouscallbacks.htm
old-project: display
ms.assetid: 9bf47408-cc7f-455d-bbb2-6f1f318eee5f
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PDD_MISCELLANEOUSCALLBACKS, DD_MISCELLANEOUSCALLBACKS, DD_MISCELLANEOUSCALLBACKS structure [Display Devices], PDD_MISCELLANEOUSCALLBACKS, PDD_MISCELLANEOUSCALLBACKS structure pointer [Display Devices], _DD_MISCELLANEOUSCALLBACKS, ddrawint/DD_MISCELLANEOUSCALLBACKS, ddrawint/PDD_MISCELLANEOUSCALLBACKS, ddstrcts_1345d66b-a9c2-497a-ba08-4fc901b24173.xml, display.dd_miscellaneouscallbacks"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.typenames: DD_MISCELLANEOUSCALLBACKS, *PDD_MISCELLANEOUSCALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddrawint.h
api_name:
-	DD_MISCELLANEOUSCALLBACKS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_MISCELLANEOUSCALLBACKS structure


## -description


The DD_MISCELLANEOUSCALLBACKS structure contains an entry pointer to the memory query callback that a device driver supports.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_MISCELLANEOUSCALLBACKS structure.


### -field dwFlags

Indicates whether the device supports the <a href="https://msdn.microsoft.com/21a1988a-1bfd-47b8-b4b6-1bc137b2ba64">DdGetAvailDriverMemory</a> callback. The driver sets this member to DDHAL_MISCCB32_GETAVAILDRIVERMEMORY when it implements the callback.


### -field GetAvailDriverMemory

Points to the driver-supplied <a href="https://msdn.microsoft.com/21a1988a-1bfd-47b8-b4b6-1bc137b2ba64">DdGetAvailDriverMemory</a> callback.


## -remarks



Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> function is called with the GUID_MiscellaneousCallbacks GUID.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550521">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551633">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551660">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551673">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551758">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/21a1988a-1bfd-47b8-b4b6-1bc137b2ba64">DdGetAvailDriverMemory</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 

