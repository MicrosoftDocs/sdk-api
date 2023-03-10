---
UID: NS:ddrawint._DD_VIDEOPORT_LOCAL
title: DD_VIDEOPORT_LOCAL (ddrawint.h)
description: The DD_VIDEOPORT_LOCAL structure contains video port extensions (VPE)-related data that is unique to an individual Microsoft DirectDraw VPE object.
helpviewer_keywords: ["*PDD_VIDEOPORT_LOCAL","DD_VIDEOPORT_LOCAL","DD_VIDEOPORT_LOCAL structure [Display Devices]","ddrawint/DD_VIDEOPORT_LOCAL","ddstrcts_ca5d2367-9338-4b1e-ad85-5c7a9e528e3e.xml","display.dd_videoport_local"]
old-location: display\dd_videoport_local.htm
tech.root: display
ms.assetid: c497d1ef-0eb1-465f-978c-60cf5606de93
ms.date: 12/05/2018
ms.keywords: '*PDD_VIDEOPORT_LOCAL, DD_VIDEOPORT_LOCAL, DD_VIDEOPORT_LOCAL structure [Display Devices], ddrawint/DD_VIDEOPORT_LOCAL, ddstrcts_ca5d2367-9338-4b1e-ad85-5c7a9e528e3e.xml, display.dd_videoport_local'
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
req.typenames: '*PDD_VIDEOPORT_LOCAL, DD_VIDEOPORT_LOCAL'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_VIDEOPORT_LOCAL
 - ddrawint/_DD_VIDEOPORT_LOCAL
 - PDD_VIDEOPORT_LOCAL
 - ddrawint/PDD_VIDEOPORT_LOCAL
 - DD_VIDEOPORT_LOCAL
 - ddrawint/DD_VIDEOPORT_LOCAL
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
 - DD_VIDEOPORT_LOCAL
---

# DD_VIDEOPORT_LOCAL structure


## -description

The DD_VIDEOPORT_LOCAL structure contains <a href="/windows-hardware/drivers/">video port extensions (VPE)</a>-related data that is unique to an individual Microsoft DirectDraw VPE object.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current DirectDraw process only.

### -field ddvpDesc

Specifies a <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportdesc">DDVIDEOPORTDESC</a> structure that describes the VPE object.

### -field ddvpInfo

Specifies a <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportinfo">DDVIDEOPORTINFO</a> structure that describes the transfer of video data to a surface.

### -field lpSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_int">DD_SURFACE_INT</a> structure for the surface receiving the video data.

### -field lpVBISurface

Points to a DD_SURFACE_INT structure for the surface receiving the <a href="/windows-hardware/drivers/">VBI</a> data.

### -field dwNumAutoflip

Specifies the number of current autoflip surfaces.

### -field dwNumVBIAutoflip

Specifies the number of VBI surfaces currently being autoflipped.

### -field dwReserved1

Reserved for use by the display driver.

### -field dwReserved2

Reserved for use by the display driver.

### -field dwReserved3

Reserved for use by the display driver.

## -remarks

This structure is initialized and filled in by DirectDraw. Except for the <b>dwReserved1</b>, <b>dwReserved2</b>, and <b>dwReserved3</b> members, the driver must not modify any other members of the DD_VIDEOPORT_LOCAL structure.