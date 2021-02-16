---
UID: NS:ddrawint._DDCOMPBUFFERINFO
title: DDCOMPBUFFERINFO (ddrawint.h)
description: The DDCOMPBUFFERINFO structure contains driver-supplied information regarding compression buffers.
helpviewer_keywords: ["*LPDDCOMPBUFFERINFO","DDCOMPBUFFERINFO","DDCOMPBUFFERINFO structure [Display Devices]","LPDDCOMPBUFFERINFO","LPDDCOMPBUFFERINFO structure pointer [Display Devices]","ddrawint/DDCOMPBUFFERINFO","ddrawint/LPDDCOMPBUFFERINFO","ddstrcts_b9871578-f3de-49fb-95f3-2668598e575a.xml","display.ddcompbufferinfo"]
old-location: display\ddcompbufferinfo.htm
tech.root: display
ms.assetid: 73dad759-499f-45b2-9345-4577deb01492
ms.date: 12/05/2018
ms.keywords: '*LPDDCOMPBUFFERINFO, DDCOMPBUFFERINFO, DDCOMPBUFFERINFO structure [Display Devices], LPDDCOMPBUFFERINFO, LPDDCOMPBUFFERINFO structure pointer [Display Devices], ddrawint/DDCOMPBUFFERINFO, ddrawint/LPDDCOMPBUFFERINFO, ddstrcts_b9871578-f3de-49fb-95f3-2668598e575a.xml, display.ddcompbufferinfo'
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
req.typenames: DDCOMPBUFFERINFO, *LPDDCOMPBUFFERINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDCOMPBUFFERINFO
 - ddrawint/_DDCOMPBUFFERINFO
 - LPDDCOMPBUFFERINFO
 - ddrawint/LPDDCOMPBUFFERINFO
 - DDCOMPBUFFERINFO
 - ddrawint/DDCOMPBUFFERINFO
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
 - DDCOMPBUFFERINFO
---

# DDCOMPBUFFERINFO structure


## -description

The DDCOMPBUFFERINFO structure contains driver-supplied information regarding compression buffers.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DDCOMPBUFFERINFO structure.

### -field dwNumCompBuffers

Indicates the number of surfaces of this type required for decompression.

### -field dwWidthToCreate

Indicates the width in pixels of the surface of this type to create.

### -field dwHeightToCreate

Indicates the height in pixels of the surface of this type to create.

### -field dwBytesToAllocate

Indicates the total number of bytes used by each surface.

### -field ddCompCaps

Points to a <a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a> structure that contains the capabilities to use when creating surfaces of this type. This allows the driver to specify the type of memory to use when creating these surfaces.

### -field ddPixelFormat

Points to a <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure that contains the pixel formats to use when creating surfaces of this type.

## -remarks

This structure passes this information to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata">DD_GETMOCOMPCOMPBUFFDATA</a> structure.