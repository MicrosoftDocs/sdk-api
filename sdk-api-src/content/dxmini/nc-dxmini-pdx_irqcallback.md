---
UID: NC:dxmini.PDX_IRQCALLBACK
title: PDX_IRQCALLBACK (dxmini.h)
description: The IRQCallback function performs operations related to the IRQ that occurred.
helpviewer_keywords: ["IRQCallback","IRQCallback callback function [Display Devices]","PDX_IRQCALLBACK","PDX_IRQCALLBACK callback","ddfncs_761fa81e-0ee5-45f4-9e33-36ecfe5c00fb.xml","display.irqcallback","dxmini/IRQCallback"]
old-location: display\irqcallback.htm
tech.root: display
ms.assetid: c4e47fb2-0d41-4efe-8f84-41e279ac8bbb
ms.date: 12/05/2018
ms.keywords: IRQCallback, IRQCallback callback function [Display Devices], PDX_IRQCALLBACK, PDX_IRQCALLBACK callback, ddfncs_761fa81e-0ee5-45f4-9e33-36ecfe5c00fb.xml, display.irqcallback, dxmini/IRQCallback
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Desktop
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDX_IRQCALLBACK
 - dxmini/PDX_IRQCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxmini.h
api_name:
 - IRQCallback
---

# PDX_IRQCALLBACK callback function


## -description

The <b>IRQCallback</b> function performs operations related to the IRQ that occurred.

## -parameters

### -param pIrqData

Points to the <a href="/windows/desktop/api/dxmini/ns-dxmini-dx_irqdata">DX_IRQDATA</a> structure that is filled in with the video miniport driver's IRQ information.

## -remarks

The <a href="/windows-hardware/drivers/display/video-miniport-drivers-in-the-windows-2000-display-driver-model">video miniport driver</a> calls the <i>IRQCallback</i> function when an IRQ occurs.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddenableirqinfo">DDENABLEIRQINFO</a>



<a href="/windows/desktop/api/dxmini/ns-dxmini-dx_irqdata">DX_IRQDATA</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_enableirq">DxEnableIRQ</a>