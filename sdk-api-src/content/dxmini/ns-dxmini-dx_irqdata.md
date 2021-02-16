---
UID: NS:dxmini._DX_IRQDATA
title: DX_IRQDATA (dxmini.h)
description: The DX_IRQDATA structure contains the IRQ information supplied by the driver.
helpviewer_keywords: ["*PDX_IRQDATA","DX_IRQDATA","DX_IRQDATA structure [Display Devices]","PDX_IRQDATA","PDX_IRQDATA structure pointer [Display Devices]","ddstrcts_abf413a4-709e-4458-930c-93f21c368892.xml","display.dx_irqdata","dxmini/DX_IRQDATA","dxmini/PDX_IRQDATA"]
old-location: display\dx_irqdata.htm
tech.root: display
ms.assetid: 258cfaa3-8de2-45d9-b61b-683cf41c127f
ms.date: 12/05/2018
ms.keywords: '*PDX_IRQDATA, DX_IRQDATA, DX_IRQDATA structure [Display Devices], PDX_IRQDATA, PDX_IRQDATA structure pointer [Display Devices], ddstrcts_abf413a4-709e-4458-930c-93f21c368892.xml, display.dx_irqdata, dxmini/DX_IRQDATA, dxmini/PDX_IRQDATA'
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
req.typenames: DX_IRQDATA, *PDX_IRQDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DX_IRQDATA
 - dxmini/_DX_IRQDATA
 - PDX_IRQDATA
 - dxmini/PDX_IRQDATA
 - DX_IRQDATA
 - dxmini/DX_IRQDATA
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
 - DX_IRQDATA
---

# DX_IRQDATA structure


## -description

The DX_IRQDATA structure contains the IRQ information supplied by the driver.

## -struct-fields

### -field dwIrqFlags

Specifies the type of IRQ that has occurred. One or more of the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDIRQ_BUSMASTER

</td>
<td>
The IRQ was generated because a transfer request was completed.

</td>
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

## -see-also

<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_irqcallback">IRQCallback</a>