---
UID: NS:ddrawint._DD_NTCALLBACKS
title: "_DD_NTCALLBACKS"
author: windows-sdk-content
description: The DD_NTCALLBACKS structure contains entry pointers to Microsoft Windows 2000 and later Microsoft DirectDraw callback functions that a device driver supports.
old-location: display\dd_ntcallbacks.htm
tech.root: Display
ms.assetid: 9d226b1c-6959-4cc8-9e60-b57a324d9a8a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDD_NTCALLBACKS, DD_NTCALLBACKS, DD_NTCALLBACKS structure [Display Devices], PDD_NTCALLBACKS, PDD_NTCALLBACKS structure pointer [Display Devices], _DD_NTCALLBACKS, ddrawint/DD_NTCALLBACKS, ddrawint/PDD_NTCALLBACKS, ddstrcts_1e79e318-f193-455c-b4c6-5f016b539207.xml, display.dd_ntcallbacks"
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
 - DD_NTCALLBACKS
product: Windows
targetos: Windows
req.typenames: DD_NTCALLBACKS, *PDD_NTCALLBACKS
req.redist: 
---

# _DD_NTCALLBACKS structure


## -description


The DD_NTCALLBACKS structure contains entry pointers to Microsoft Windows 2000 and later Microsoft DirectDraw callback functions that a device driver supports.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_NTCALLBACKS structure.


### -field dwFlags

Indicates what Windows 2000 and later callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_NTCB32_FREEDRIVERMEMORY</dt>
<dt>DDHAL_NTCB32_SETEXCLUSIVEMODE</dt>
<dt>DDHAL_NTCB32_FLIPTOGDISURFACE</dt>
</dl>



### -field FreeDriverMemory

Points to the driver-supplied <a href="https://msdn.microsoft.com/dd37c6b5-2039-487f-badc-840ac6cc7906">DdFreeDriverMemory</a> callback.


### -field SetExclusiveMode

Points to the driver-supplied <a href="https://msdn.microsoft.com/c322a4ac-0900-4f31-9e02-923afdad5fd6">DdSetExclusiveMode</a> callback.


### -field FlipToGDISurface

Points to the driver-supplied <a href="https://msdn.microsoft.com/279987bb-1697-4157-9d61-d503b0183e84">DdFlipToGDISurface</a> callback.


## -remarks



Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> function is called with the GUID_NTCallbacks GUID.




## -see-also




<a href="https://msdn.microsoft.com/fcf0e136-a7cc-4bb3-8af4-2478d4a2c055">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/85dcb71b-ad1f-4b83-8ead-db502d9f294e">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/9bf47408-cc7f-455d-bbb2-6f1f318eee5f">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/db707fd8-2190-4c4f-89fd-ab46d97f66a2">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/742b03b0-f729-489c-a87f-b8eb404b6290">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/a363446e-a9f7-4b32-acc2-c369d3dfe8f3">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/5e03d240-f483-4ecf-8890-b9f0368e2b2f">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/279987bb-1697-4157-9d61-d503b0183e84">DdFlipToGDISurface</a>



<a href="https://msdn.microsoft.com/dd37c6b5-2039-487f-badc-840ac6cc7906">DdFreeDriverMemory</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>



<a href="https://msdn.microsoft.com/c322a4ac-0900-4f31-9e02-923afdad5fd6">DdSetExclusiveMode</a>
 

 

