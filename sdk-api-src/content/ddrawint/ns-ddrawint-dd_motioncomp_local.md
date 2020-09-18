---
UID: NS:ddrawint._DD_MOTIONCOMP_LOCAL
title: DD_MOTIONCOMP_LOCAL (ddrawint.h)
description: The DD_MOTIONCOMP_LOCAL structure contains local data for each individual Microsoft DirectDraw motion compensation object.
helpviewer_keywords: ["*PDD_MOTIONCOMP_LOCAL","DD_MOTIONCOMP_LOCAL","DD_MOTIONCOMP_LOCAL structure [Display Devices]","ddrawint/DD_MOTIONCOMP_LOCAL","ddstrcts_cc4890b6-b2b6-484c-b979-4627fa902d7d.xml","display.dd_motioncomp_local"]
old-location: display\dd_motioncomp_local.htm
tech.root: display
ms.assetid: 41cde03a-f9da-4701-a0df-0dba0c17ba26
ms.date: 12/05/2018
ms.keywords: '*PDD_MOTIONCOMP_LOCAL, DD_MOTIONCOMP_LOCAL, DD_MOTIONCOMP_LOCAL structure [Display Devices], ddrawint/DD_MOTIONCOMP_LOCAL, ddstrcts_cc4890b6-b2b6-484c-b979-4627fa902d7d.xml, display.dd_motioncomp_local'
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
req.typenames: '*PDD_MOTIONCOMP_LOCAL, DD_MOTIONCOMP_LOCAL'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_MOTIONCOMP_LOCAL
 - ddrawint/_DD_MOTIONCOMP_LOCAL
 - PDD_MOTIONCOMP_LOCAL
 - ddrawint/PDD_MOTIONCOMP_LOCAL
 - DD_MOTIONCOMP_LOCAL
 - ddrawint/DD_MOTIONCOMP_LOCAL
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
 - DD_MOTIONCOMP_LOCAL
---

# DD_MOTIONCOMP_LOCAL structure


## -description

The DD_MOTIONCOMP_LOCAL structure contains local data for each individual Microsoft DirectDraw motion compensation object.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current DirectDraw process only.

### -field guid

Specifies a GUID that describes the motion compensation process being used.

### -field dwUncompWidth

Indicates the width in pixels of the uncompressed output frame.

### -field dwUncompHeight

Indicates the height in pixels of the uncompressed output frame.

### -field ddUncompPixelFormat

Specifies a <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure that contains the pixel format of the uncompressed output frame.

### -field dwDriverReserved1

### -field dwDriverReserved2

### -field dwDriverReserved3

Are reserved for use by the display driver.

### -field lpDriverReserved1

### -field lpDriverReserved2

### -field lpDriverReserved3

Are reserved for use by the display driver.