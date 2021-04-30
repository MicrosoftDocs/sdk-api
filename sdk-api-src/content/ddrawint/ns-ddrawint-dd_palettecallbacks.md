---
UID: NS:ddrawint.DD_PALETTECALLBACKS
title: DD_PALETTECALLBACKS (ddrawint.h)
description: The DD_PALETTECALLBACKS structure contains entry pointers to the DirectDraw palette callback functions that a device driver supports.
helpviewer_keywords: ["*PDD_PALETTECALLBACKS","DD_PALETTECALLBACKS","DD_PALETTECALLBACKS structure [Display Devices]","PDD_PALETTECALLBACKS","PDD_PALETTECALLBACKS structure pointer [Display Devices]","ddrawint/DD_PALETTECALLBACKS","ddrawint/PDD_PALETTECALLBACKS","ddstrcts_def94357-6d48-46e6-848a-ef85f13de99e.xml","display.dd_palettecallbacks"]
old-location: display\dd_palettecallbacks.htm
tech.root: display
ms.assetid: 742b03b0-f729-489c-a87f-b8eb404b6290
ms.date: 12/05/2018
ms.keywords: '*PDD_PALETTECALLBACKS, DD_PALETTECALLBACKS, DD_PALETTECALLBACKS structure [Display Devices], PDD_PALETTECALLBACKS, PDD_PALETTECALLBACKS structure pointer [Display Devices], ddrawint/DD_PALETTECALLBACKS, ddrawint/PDD_PALETTECALLBACKS, ddstrcts_def94357-6d48-46e6-848a-ef85f13de99e.xml, display.dd_palettecallbacks'
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
targetos: Windows
req.typenames: DD_PALETTECALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DD_PALETTECALLBACKS
 - ddrawint/DD_PALETTECALLBACKS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_PALETTECALLBACKS
---

# DD_PALETTECALLBACKS structure


## -description

The DD_PALETTECALLBACKS structure contains entry pointers to the DirectDraw palette callback functions that a device driver supports.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DD_PALETTECALLBACKS structure.

### -field dwFlags

Indicates what DirectDrawPalette callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_PALCB32_DESTROYPALETTE</dt>
<dt>DDHAL_PALCB32_SETENTRIES</dt>
</dl>

### -field DestroyPalette

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_palcb_destroypalette">DdDestroyPalette</a> palette callback.

### -field SetEntries

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_palcb_setentries">DdSetEntries</a> palette callback.

## -remarks

Entries that the display driver does not use should be set to <b>NULL</b>. The driver initializes this structure in <a href="/windows/desktop/api/winddi/nf-winddi-drvenabledirectdraw">DrvEnableDirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontrolcallbacks">DD_COLORCONTROLCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_kernelcallbacks">DD_KERNELCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_miscellaneouscallbacks">DD_MISCELLANEOUSCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncompcallbacks">DD_MOTIONCOMPCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_ntcallbacks">DD_NTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoportcallbacks">DD_VIDEOPORTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_palcb_destroypalette">DdDestroyPalette</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_palcb_setentries">DdSetEntries</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenabledirectdraw">DrvEnableDirectDraw</a>