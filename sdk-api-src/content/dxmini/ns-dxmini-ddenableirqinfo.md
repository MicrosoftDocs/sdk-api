---
UID: NS:dxmini._DDENABLEIRQINFO
title: DDENABLEIRQINFO (dxmini.h)
description: The DDENABLEIRQINFO structure contains the information required to enable interrupts.
helpviewer_keywords: ["*PDDENABLEIRQINFO","DDENABLEIRQINFO","DDENABLEIRQINFO structure [Display Devices]","PDDENABLEIRQINFO","PDDENABLEIRQINFO structure pointer [Display Devices]","Video_Structs_8d9ac070-bb9e-4cc4-af09-9e8f7942516f.xml","display.ddenableirqinfo","dxmini/DDENABLEIRQINFO","dxmini/PDDENABLEIRQINFO"]
old-location: display\ddenableirqinfo.htm
tech.root: display
ms.assetid: f6ac3ef8-1afc-4c0f-b24f-34d3d56d62a8
ms.date: 12/05/2018
ms.keywords: '*PDDENABLEIRQINFO, DDENABLEIRQINFO, DDENABLEIRQINFO structure [Display Devices], PDDENABLEIRQINFO, PDDENABLEIRQINFO structure pointer [Display Devices], Video_Structs_8d9ac070-bb9e-4cc4-af09-9e8f7942516f.xml, display.ddenableirqinfo, dxmini/DDENABLEIRQINFO, dxmini/PDDENABLEIRQINFO'
req.header: dxmini.h
req.include-header: Dxmini.h
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
req.typenames: DDENABLEIRQINFO, *PDDENABLEIRQINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDENABLEIRQINFO
 - dxmini/_DDENABLEIRQINFO
 - PDDENABLEIRQINFO
 - dxmini/PDDENABLEIRQINFO
 - DDENABLEIRQINFO
 - dxmini/DDENABLEIRQINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDENABLEIRQINFO
---

# DDENABLEIRQINFO structure


## -description

The DDENABLEIRQINFO structure contains the information required to enable interrupts.

## -struct-fields

### -field dwIRQSources

Indicates the interrupts that should be enabled. This member can be one or more of the following values: 

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
The device can generate IRQs based on the display V-sync.

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
The device can generate V-sync IRQs for hardware video port number 0.

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
The device can generate V-sync IRQs for hardware video port number 1.

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
The device can generate IRQs based on a programmable line for hardware video port number 9.

</td>
</tr>
<tr>
<td>
DDIRQ_VPORT9_VSYNC

</td>
<td>
The device can generate V-sync IRQs for hardware video port number 9.

</td>
</tr>
</table>

### -field dwLine

Indicates which line should generate the IRQ. If the hardware does not have the ability to generate an IRQ based on a programmable line, the value in this member is meaningless.

### -field IRQCallback

Points to an <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_irqcallback">IRQCallback</a> that the video miniport driver calls when the miniport driver is managing IRQs, and an IRQ occurs.

### -field lpIRQData

Points to the data to be sent to <b>IRQCallback</b> when <b>IRQCallback</b> is called.

## -remarks

The <b>dwIRQSources</b> member of this structure does not use the DDIRQ_BUSMASTER flag. However, the DDIRQ_BUSMASTER flag can be set in the <b>dwIrqFlags</b> member of the <a href="/windows/desktop/api/dxmini/ns-dxmini-dx_irqdata">DX_IRQDATA</a> structure. The driver passes this DX_IRQDATA to the <b>IRQCallback</b> function when an IRQ occurs.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-dx_irqdata">DX_IRQDATA</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_enableirq">DxEnableIRQ</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_irqcallback">IRQCallback</a>