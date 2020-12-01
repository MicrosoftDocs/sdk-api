---
UID: NS:ddrawint._DD_COLORCONTROLCALLBACKS
title: DD_COLORCONTROLCALLBACKS (ddrawint.h)
description: The DD_COLORCONTROLCALLBACKS structure contains an entry pointer to the Microsoft DirectDraw color control callback that a device driver supports.
helpviewer_keywords: ["*PDD_COLORCONTROLCALLBACKS","DD_COLORCONTROLCALLBACKS","DD_COLORCONTROLCALLBACKS structure [Display Devices]","PDD_COLORCONTROLCALLBACKS","PDD_COLORCONTROLCALLBACKS structure pointer [Display Devices]","ddrawint/DD_COLORCONTROLCALLBACKS","ddrawint/PDD_COLORCONTROLCALLBACKS","ddstrcts_2e14797b-2bd8-4107-8085-60f8b5838bda.xml","display.dd_colorcontrolcallbacks"]
old-location: display\dd_colorcontrolcallbacks.htm
tech.root: display
ms.assetid: fcf0e136-a7cc-4bb3-8af4-2478d4a2c055
ms.date: 12/05/2018
ms.keywords: '*PDD_COLORCONTROLCALLBACKS, DD_COLORCONTROLCALLBACKS, DD_COLORCONTROLCALLBACKS structure [Display Devices], PDD_COLORCONTROLCALLBACKS, PDD_COLORCONTROLCALLBACKS structure pointer [Display Devices], ddrawint/DD_COLORCONTROLCALLBACKS, ddrawint/PDD_COLORCONTROLCALLBACKS, ddstrcts_2e14797b-2bd8-4107-8085-60f8b5838bda.xml, display.dd_colorcontrolcallbacks'
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
req.typenames: DD_COLORCONTROLCALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_COLORCONTROLCALLBACKS
 - ddrawint/_DD_COLORCONTROLCALLBACKS
 - DD_COLORCONTROLCALLBACKS
 - ddrawint/DD_COLORCONTROLCALLBACKS
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
 - DD_COLORCONTROLCALLBACKS
---

# DD_COLORCONTROLCALLBACKS structure


## -description

The DD_COLORCONTROLCALLBACKS structure contains an entry pointer to the Microsoft DirectDraw color control callback that a device driver supports.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DD_COLORCONTROLCALLBACKS structure.

### -field dwFlags

Indicates whether the device supports the color control callback identified by <b>ColorControl</b>. The driver should set this member to be DDHAL_COLOR_COLORCONTROL when it implements the color control callback.

### -field ColorControl

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_colorcb_colorcontrol">DdControlColor</a> callback.

## -remarks

Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> function is called with the GUID_ColorControlCallbacks GUID.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_callbacks">DD_CALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_kernelcallbacks">DD_KERNELCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_miscellaneouscallbacks">DD_MISCELLANEOUSCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncompcallbacks">DD_MOTIONCOMPCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_ntcallbacks">DD_NTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoportcallbacks">DD_VIDEOPORTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_colorcb_colorcontrol">DdControlColor</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>