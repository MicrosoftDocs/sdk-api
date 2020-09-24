---
UID: NS:ddrawint._DD_STEREOMODE
title: DD_STEREOMODE (ddrawint.h)
description: The DD_STEREOMODE structure is used by the runtime with GUID_DDStereoMode in a DdGetDriverInfo call to query whether the driver supports stereo for a given video display mode.
helpviewer_keywords: ["*PDD_STEREOMODE","DD_STEREOMODE","DD_STEREOMODE structure [Display Devices]","ddrawint/DD_STEREOMODE","ddstrcts_aca080e5-a3ae-409b-9546-f4d270fb9f10.xml","display.dd_stereomode"]
old-location: display\dd_stereomode.htm
tech.root: display
ms.assetid: 0b160c57-5e79-4777-a514-fa04e02c1508
ms.date: 12/05/2018
ms.keywords: '*PDD_STEREOMODE, DD_STEREOMODE, DD_STEREOMODE structure [Display Devices], ddrawint/DD_STEREOMODE, ddstrcts_aca080e5-a3ae-409b-9546-f4d270fb9f10.xml, display.dd_stereomode'
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
req.typenames: '*PDD_STEREOMODE, DD_STEREOMODE'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_STEREOMODE
 - ddrawint/_DD_STEREOMODE
 - PDD_STEREOMODE
 - ddrawint/PDD_STEREOMODE
 - DD_STEREOMODE
 - ddrawint/DD_STEREOMODE
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
 - DD_STEREOMODE
---

# DD_STEREOMODE structure


## -description

The DD_STEREOMODE structure is used by the runtime with GUID_DDStereoMode in a <b>DdGetDriverInfo</b> call to query whether the driver supports stereo for a given video display mode.

## -struct-fields

### -field dwSize

Specifies the size in bytes of the DD_STEREOMODE structure.

### -field dwHeight

Specifies the height in scan lines of the display mode. Has the value D3DGDI2_MAGIC if this structure is, in fact, a <a href="/windows-hardware/drivers/ddi/content/d3dhal/ns-d3dhal-_dd_getdriverinfo2data">DD_GETDRIVERINFO2DATA</a> call.

### -field dwWidth

Specifies the width in pixels of the display mode.

### -field dwBpp

Specifies the bits per pixel of the display mode.

### -field dwRefreshRate

Specifies the refresh rate in hertz of the display mode.

### -field bSupported

Driver sets to <b>TRUE</b> if stereo is supported with the specified display mode, or <b>FALSE</b> otherwise.

## -remarks

To check each display mode to see if the driver supports stereo with that mode, the runtime calls the driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> function. In this call, the runtime specifies GUID_DDStereoMode in the <b>guidInfo</b> member of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getdriverinfodata">DD_GETDRIVERINFODATA</a> structure to which the <i>lpGetDriverInfo</i> parameter points. The runtime also provides a pointer to a DD_STEREOMODE structure in the <b>lpvData</b> member of DD_GETDRIVERINFODATA. The driver returns DD_OK if it supports GUID_DDStereoMode and sets the <b>bSupported</b> member of DD_STEREOMODE to <b>TRUE</b> if it supports stereo with the specified display mode.

GUID_DDStereoMode provides a way to turn OFF stereo per-mode, since it is expected that a driver that can do stereo can do stereo in any mode.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/d3dhal/ns-d3dhal-_dd_getdriverinfo2data">DD_GETDRIVERINFO2DATA</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getdriverinfodata">DD_GETDRIVERINFODATA</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>