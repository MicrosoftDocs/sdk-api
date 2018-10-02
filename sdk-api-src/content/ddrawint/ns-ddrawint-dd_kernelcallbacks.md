---
UID: NS:ddrawint.DD_KERNELCALLBACKS
title: DD_KERNELCALLBACKS
author: windows-sdk-content
description: The DD_KERNELCALLBACKS structure contains entry pointers to the DirectDraw kernel-mode callback functions that the driver supports.
old-location: display\dd_kernelcallbacks.htm
tech.root: Display
ms.assetid: 85dcb71b-ad1f-4b83-8ead-db502d9f294e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDD_KERNELCALLBACKS, DD_KERNELCALLBACKS, DD_KERNELCALLBACKS structure [Display Devices], PDD_KERNELCALLBACKS, PDD_KERNELCALLBACKS structure pointer [Display Devices], ddrawint/DD_KERNELCALLBACKS, ddrawint/PDD_KERNELCALLBACKS, ddstrcts_6d33c1f1-37e3-421a-b40f-1009a5ee3d25.xml, display.dd_kernelcallbacks"
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
 - DD_KERNELCALLBACKS
product: Windows
targetos: Windows
req.typenames: DD_KERNELCALLBACKS, *PDD_KERNELCALLBACKS
req.redist: 
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




<a href="https://msdn.microsoft.com/fcf0e136-a7cc-4bb3-8af4-2478d4a2c055">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/9bf47408-cc7f-455d-bbb2-6f1f318eee5f">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/db707fd8-2190-4c4f-89fd-ab46d97f66a2">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/9d226b1c-6959-4cc8-9e60-b57a324d9a8a">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/742b03b0-f729-489c-a87f-b8eb404b6290">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/a363446e-a9f7-4b32-acc2-c369d3dfe8f3">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/5e03d240-f483-4ecf-8890-b9f0368e2b2f">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>



<a href="https://msdn.microsoft.com/730e0fd4-aaae-4de7-86d5-fa2145be3cd1">DdSyncSurfaceData</a>



<a href="https://msdn.microsoft.com/3726a505-c3cf-4784-886e-2f4524fb0c5b">DdSyncVideoPortData</a>
 

 

