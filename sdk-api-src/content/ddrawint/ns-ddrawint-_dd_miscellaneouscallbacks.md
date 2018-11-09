---
UID: NS:ddrawint._DD_MISCELLANEOUSCALLBACKS
title: "_DD_MISCELLANEOUSCALLBACKS"
author: windows-sdk-content
description: The DD_MISCELLANEOUSCALLBACKS structure contains an entry pointer to the memory query callback that a device driver supports.
old-location: display\dd_miscellaneouscallbacks.htm
tech.root: display
ms.assetid: 9bf47408-cc7f-455d-bbb2-6f1f318eee5f
ms.author: windowssdkdev
ms.date: 11/02/2018
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_MISCELLANEOUSCALLBACKS
product: Windows
targetos: Windows
req.typenames: DD_MISCELLANEOUSCALLBACKS, *PDD_MISCELLANEOUSCALLBACKS
req.redist: 
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




<a href="https://msdn.microsoft.com/fcf0e136-a7cc-4bb3-8af4-2478d4a2c055">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/85dcb71b-ad1f-4b83-8ead-db502d9f294e">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/db707fd8-2190-4c4f-89fd-ab46d97f66a2">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/9d226b1c-6959-4cc8-9e60-b57a324d9a8a">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/742b03b0-f729-489c-a87f-b8eb404b6290">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/a363446e-a9f7-4b32-acc2-c369d3dfe8f3">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/5e03d240-f483-4ecf-8890-b9f0368e2b2f">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/21a1988a-1bfd-47b8-b4b6-1bc137b2ba64">DdGetAvailDriverMemory</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 

