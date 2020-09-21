---
UID: NS:ddrawint._DD_MISCELLANEOUSCALLBACKS
title: DD_MISCELLANEOUSCALLBACKS (ddrawint.h)
description: The DD_MISCELLANEOUSCALLBACKS structure contains an entry pointer to the memory query callback that a device driver supports.
helpviewer_keywords: ["*PDD_MISCELLANEOUSCALLBACKS","DD_MISCELLANEOUSCALLBACKS","DD_MISCELLANEOUSCALLBACKS structure [Display Devices]","PDD_MISCELLANEOUSCALLBACKS","PDD_MISCELLANEOUSCALLBACKS structure pointer [Display Devices]","ddrawint/DD_MISCELLANEOUSCALLBACKS","ddrawint/PDD_MISCELLANEOUSCALLBACKS","ddstrcts_1345d66b-a9c2-497a-ba08-4fc901b24173.xml","display.dd_miscellaneouscallbacks"]
old-location: display\dd_miscellaneouscallbacks.htm
tech.root: display
ms.assetid: 9bf47408-cc7f-455d-bbb2-6f1f318eee5f
ms.date: 12/05/2018
ms.keywords: '*PDD_MISCELLANEOUSCALLBACKS, DD_MISCELLANEOUSCALLBACKS, DD_MISCELLANEOUSCALLBACKS structure [Display Devices], PDD_MISCELLANEOUSCALLBACKS, PDD_MISCELLANEOUSCALLBACKS structure pointer [Display Devices], ddrawint/DD_MISCELLANEOUSCALLBACKS, ddrawint/PDD_MISCELLANEOUSCALLBACKS, ddstrcts_1345d66b-a9c2-497a-ba08-4fc901b24173.xml, display.dd_miscellaneouscallbacks'
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
req.typenames: DD_MISCELLANEOUSCALLBACKS, *PDD_MISCELLANEOUSCALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_MISCELLANEOUSCALLBACKS
 - ddrawint/_DD_MISCELLANEOUSCALLBACKS
 - PDD_MISCELLANEOUSCALLBACKS
 - ddrawint/PDD_MISCELLANEOUSCALLBACKS
 - DD_MISCELLANEOUSCALLBACKS
 - ddrawint/DD_MISCELLANEOUSCALLBACKS
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
 - DD_MISCELLANEOUSCALLBACKS
---

# DD_MISCELLANEOUSCALLBACKS structure


## -description

The DD_MISCELLANEOUSCALLBACKS structure contains an entry pointer to the memory query callback that a device driver supports.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DD_MISCELLANEOUSCALLBACKS structure.

### -field dwFlags

Indicates whether the device supports the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getavaildrivermemory">DdGetAvailDriverMemory</a> callback. The driver sets this member to DDHAL_MISCCB32_GETAVAILDRIVERMEMORY when it implements the callback.

### -field GetAvailDriverMemory

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getavaildrivermemory">DdGetAvailDriverMemory</a> callback.

## -remarks

Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> function is called with the GUID_MiscellaneousCallbacks GUID.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontrolcallbacks">DD_COLORCONTROLCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_kernelcallbacks">DD_KERNELCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncompcallbacks">DD_MOTIONCOMPCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_ntcallbacks">DD_NTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoportcallbacks">DD_VIDEOPORTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getavaildrivermemory">DdGetAvailDriverMemory</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>