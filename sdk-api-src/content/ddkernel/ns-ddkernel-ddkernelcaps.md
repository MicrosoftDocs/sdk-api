---
UID: NS:ddkernel._DDKERNELCAPS
title: DDKERNELCAPS (ddkernel.h)
description: The DDKERNELCAPS structure notifies the client what support, if any, exists in the miniport driver for the kernel-mode video transport.
helpviewer_keywords: ["*LPDDKERNELCAPS","DDKERNELCAPS","DDKERNELCAPS structure [Display Devices]","LPDDKERNELCAPS","LPDDKERNELCAPS structure pointer [Display Devices]","ddkernel/DDKERNELCAPS","ddkernel/LPDDKERNELCAPS","ddstrcts_efe32a57-5435-4e15-a17f-880870d70c85.xml","display.ddkernelcaps"]
old-location: display\ddkernelcaps.htm
tech.root: display
ms.assetid: d02d26f5-34cf-4a3c-b67c-0f9191bb854b
ms.date: 12/05/2018
ms.keywords: '*LPDDKERNELCAPS, DDKERNELCAPS, DDKERNELCAPS structure [Display Devices], LPDDKERNELCAPS, LPDDKERNELCAPS structure pointer [Display Devices], ddkernel/DDKERNELCAPS, ddkernel/LPDDKERNELCAPS, ddstrcts_efe32a57-5435-4e15-a17f-880870d70c85.xml, display.ddkernelcaps'
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
targetos: Windows
req.typenames: '*LPDDKERNELCAPS, DDKERNELCAPS'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDKERNELCAPS
 - ddkernel/_DDKERNELCAPS
 - LPDDKERNELCAPS
 - ddkernel/LPDDKERNELCAPS
 - DDKERNELCAPS
 - ddkernel/DDKERNELCAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkernel.h
api_name:
 - DDKERNELCAPS
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
The driver supports the <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_flipvideoport">DxFlipVideoPort</a> and the <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_flipoverlay">DxFlipOverlay</a> callbacks, and that these callbacks can be used for autoflipping.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_CAPTURE_INVERTED

</td>
<td>
The device supports inverting the <a href="/windows-hardware/drivers/">DIBs</a> while capturing the data.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_CAPTURE_NONLOCALVIDMEM

</td>
<td>
The device supports a <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> capture interface capable of transferring data to nonlocal display memory.

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
The driver supports the <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_flipoverlay">DxFlipOverlay</a> callback.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_FLIPVIDEOPORT

</td>
<td>
The driver supports the <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_flipvideoport">DxFlipVideoPort</a> callback.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_LOCK

</td>
<td>
The device supports accessing the frame buffer without causing contention with blitters, and so on, and that the driver supports the <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_lock">DxLock</a> callback.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_SETSTATE

</td>
<td>
The driver supports the <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_setstate">DxSetState</a> callback, allowing a client to switch between bob and weave display modes.

</td>
</tr>
<tr>
<td>
DDKERNELCAPS_SKIPFIELDS

</td>
<td>
The device supports field skipping, either using hardware or by supporting the <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_skipnextfield">DxSkipNextField</a> callback.

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

<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_flipoverlay">DxFlipOverlay</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_flipvideoport">DxFlipVideoPort</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_lock">DxLock</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_setstate">DxSetState</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_skipnextfield">DxSkipNextField</a>