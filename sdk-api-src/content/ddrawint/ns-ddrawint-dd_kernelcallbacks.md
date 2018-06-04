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

# DD_KERNELCALLBACKS structure


## -description


The DD_KERNELCALLBACKS structure contains entry pointers to the DirectDraw kernel-mode callback functions that the driver supports.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_KERNELCALLBACKS structure.


### -field dwFlags

Indicates what Microsoft DirectDraw kernel callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_KERNEL_SYNCSURFACEDATA </dt>
<dt>DDHAL_KERNEL_SYNCVIDEOPORTDATA </dt>
</dl>



### -field SyncSurfaceData

Points to the driver-supplied <a href="https://msdn.microsoft.com/730e0fd4-aaae-4de7-86d5-fa2145be3cd1">DdSyncSurfaceData</a> callback.


### -field SyncVideoPortData

Points to the driver-supplied <a href="https://msdn.microsoft.com/3726a505-c3cf-4784-886e-2f4524fb0c5b">DdSyncVideoPortData</a> callback. 


## -remarks



Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> function is called with the GUID_KernelCallbacks GUID.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550521">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551657">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551660">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551673">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551758">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>



<a href="https://msdn.microsoft.com/730e0fd4-aaae-4de7-86d5-fa2145be3cd1">DdSyncSurfaceData</a>



<a href="https://msdn.microsoft.com/3726a505-c3cf-4784-886e-2f4524fb0c5b">DdSyncVideoPortData</a>
 

 

