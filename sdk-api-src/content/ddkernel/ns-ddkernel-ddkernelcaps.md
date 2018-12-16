---
UID: NS:ddkernel._DDKERNELCAPS
title: DDKERNELCAPS
author: windows-sdk-content
description: The DDKERNELCAPS structure notifies the client what support, if any, exists in the miniport driver for the kernel-mode video transport.
old-location: display\ddkernelcaps.htm
tech.root: display
ms.assetid: d02d26f5-34cf-4a3c-b67c-0f9191bb854b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDDKERNELCAPS, DDKERNELCAPS, DDKERNELCAPS structure [Display Devices], LPDDKERNELCAPS, LPDDKERNELCAPS structure pointer [Display Devices], ddkernel/DDKERNELCAPS, ddkernel/LPDDKERNELCAPS, ddstrcts_efe32a57-5435-4e15-a17f-880870d70c85.xml, display.ddkernelcaps"
ms.topic: struct
req.header: ddkernel.h
req.include-header: Ddkernel.h
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
 - ddkernel.h
api_name:
 - DDKERNELCAPS
product: Windows
targetos: Windows
req.typenames: "*LPDDKERNELCAPS, DDKERNELCAPS"
req.redist: 
---

# DDKERNELCAPS structure


## -description


The DDKERNELCAPS structure notifies the client what support, if any, exists in the miniport driver for the kernel-mode video transport. 


## -struct-fields




### -field dwSize

Specifies the size, in bytes, of this structure. This member must be initialized before the structure is used. 


### -field dwCaps

Specifies a set of flags indicating the device's capabilities. This member can be any combination of the following capabilities: 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDKERNELCAPS_AUTOFLIP

</td>
<td>
The driver supports the <a href="https://msdn.microsoft.com/d6047c90-1163-475a-a55b-95ccb0570e3e">DxFlipVideoPort</a> and the <a href="https://msdn.microsoft.com/7674f853-e5ea-44c7-b5ed-5fd90bfa1bcb">DxFlipOverlay</a> callbacks, and that these callbacks can be used for autoflipping.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_CAPTURE_INVERTED

</td>
<td>
The device supports inverting the <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">DIBs</a> while capturing the data.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_CAPTURE_NONLOCALVIDMEM

</td>
<td>
The device supports a <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> capture interface capable of transferring data to nonlocal display memory.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_CAPTURE_SYSMEM

</td>
<td>
The device supports a VPE capture interface capable of transferring data to system memory.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_FIELDPOLARITY

</td>
<td>
The device can report the polarity (even/odd) of the current VPE object field.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_FLIPOVERLAY

</td>
<td>
The driver supports the <a href="https://msdn.microsoft.com/7674f853-e5ea-44c7-b5ed-5fd90bfa1bcb">DxFlipOverlay</a> callback.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_FLIPVIDEOPORT

</td>
<td>
The driver supports the <a href="https://msdn.microsoft.com/d6047c90-1163-475a-a55b-95ccb0570e3e">DxFlipVideoPort</a> callback.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_LOCK

</td>
<td>
The device supports accessing the frame buffer without causing contention with blitters, and so on, and that the driver supports the <a href="https://msdn.microsoft.com/1eeeb68b-9098-4030-924a-634e79c3e682">DxLock</a> callback.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_SETSTATE

</td>
<td>
The driver supports the <a href="https://msdn.microsoft.com/f2d7f248-017e-4375-b0a0-49de65192511">DxSetState</a> callback, allowing a client to switch between bob and weave display modes.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_SKIPFIELDS

</td>
<td>
The device supports field skipping, either using hardware or by supporting the <a href="https://msdn.microsoft.com/da19c8dc-fef5-41e6-b032-2a0ae05a73da">DxSkipNextField</a> callback.

</td>
</tr>
</table>
 


### -field dwIRQCaps

Can be a combination of the following flags: 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDIRQ_DISPLAY_VSYNC

</td>
<td>
The device can generate IRQs based on the display VSYNC.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT0_LINE

</td>
<td>
The device can generate IRQs based on a programmable line for hardware video port number 0. 

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT0_VSYNC

</td>
<td>
The device can generate VSYNC IRQs for hardware video port number 0. 

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT1_LINE

</td>
<td>
The device can generate IRQs based on a programmable line for hardware video port number 1.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT1_VSYNC

</td>
<td>
The device can generate V-sync IRQs for hardware video port number 1

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT2_LINE

</td>
<td>
The device can generate IRQs based on a programmable line for hardware video port number 2.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT2_VSYNC

</td>
<td>
The device can generate V-sync IRQs for hardware video port number 2.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT3_LINE

</td>
<td>
The device can generate IRQs based on a programmable line for hardware video port number 3.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT3_VSYNC

</td>
<td>
The device can generate V-sync IRQs for hardware video port number 3.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT4_LINE

</td>
<td>
The device can generate IRQs based on a programmable line for hardware video port number 4.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT4_VSYNC

</td>
<td>
The device can generate V-sync IRQs for hardware video port number 4.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT5_LINE

</td>
<td>
The device can generate IRQs based on a programmable line for hardware video port number 5.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT5_VSYNC

</td>
<td>
The device can generate V-sync IRQs for hardware video port number 5.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT6_LINE

</td>
<td>
The device can generate IRQs based on a programmable line for hardware video port number 6.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT6_VSYNC

</td>
<td>
The device can generate V-sync IRQs for hardware video port number 6.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT7_LINE

</td>
<td>
The device can generate IRQs based on a programmable line for hardware video port number 7.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT7_VSYNC

</td>
<td>
The device can generate V-sync IRQs for hardware video port number 7.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT8_LINE

</td>
<td>
The device can generate IRQs based on a programmable line for hardware video port number 8.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT8_VSYNC

</td>
<td>
The device can generate V-sync IRQs for hardware video port number 8.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT9_LINE

</td>
<td>
he device can generate IRQs based on a programmable line for hardware video port number 9.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT9_VSYNC

</td>
<td>
he device can generate V-sync IRQs for hardware video port number 9.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/7674f853-e5ea-44c7-b5ed-5fd90bfa1bcb">DxFlipOverlay</a>



<a href="https://msdn.microsoft.com/d6047c90-1163-475a-a55b-95ccb0570e3e">DxFlipVideoPort</a>



<a href="https://msdn.microsoft.com/1eeeb68b-9098-4030-924a-634e79c3e682">DxLock</a>



<a href="https://msdn.microsoft.com/f2d7f248-017e-4375-b0a0-49de65192511">DxSetState</a>



<a href="https://msdn.microsoft.com/da19c8dc-fef5-41e6-b032-2a0ae05a73da">DxSkipNextField</a>
 

 

