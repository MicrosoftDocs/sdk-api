---
UID: NS:ddrawint._DD_DESTROYSURFACEDATA
title: DD_DESTROYSURFACEDATA (ddrawint.h)
description: The DD_DESTROYSURFACEDATA structure contains information necessary to destroy the specified surface--in the case of DestroyD3DBuffer, a command or vertex buffer.
helpviewer_keywords: ["*PDD_DESTROYSURFACEDATA","DD_DESTROYSURFACEDATA","DD_DESTROYSURFACEDATA structure [Display Devices]","ddrawint/DD_DESTROYSURFACEDATA","ddstrcts_19c2445b-0f9f-445d-a486-8ca100beeca7.xml","display.dd_destroysurfacedata"]
old-location: display\dd_destroysurfacedata.htm
tech.root: display
ms.assetid: 77d9544d-72df-4e7d-ba57-644aeee34a88
ms.date: 12/05/2018
ms.keywords: '*PDD_DESTROYSURFACEDATA, DD_DESTROYSURFACEDATA, DD_DESTROYSURFACEDATA structure [Display Devices], ddrawint/DD_DESTROYSURFACEDATA, ddstrcts_19c2445b-0f9f-445d-a486-8ca100beeca7.xml, display.dd_destroysurfacedata'
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
req.typenames: '*PDD_DESTROYSURFACEDATA, DD_DESTROYSURFACEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_DESTROYSURFACEDATA
 - ddrawint/_DD_DESTROYSURFACEDATA
 - PDD_DESTROYSURFACEDATA
 - ddrawint/PDD_DESTROYSURFACEDATA
 - DD_DESTROYSURFACEDATA
 - ddrawint/DD_DESTROYSURFACEDATA
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
 - DD_DESTROYSURFACEDATA
---

# DD_DESTROYSURFACEDATA structure


## -description

The DD_DESTROYSURFACEDATA structure contains information necessary to destroy the specified surface--in the case of <a href="/previous-versions/windows/hardware/drivers/ff552754(v=vs.85)">DestroyD3DBuffer</a>, a command or vertex buffer.

## -struct-fields

### -field lpDD

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSurface

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure representing the surface or buffer object to be destroyed.

### -field ddRVal

Specifies the location in which the driver writes the return value of either the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_destroysurface">DdDestroySurface</a> or <a href="/previous-versions/windows/hardware/drivers/ff552754(v=vs.85)">DestroyD3DBuffer</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field DestroySurface

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_destroysurface">DdDestroySurface</a>



<a href="/previous-versions/windows/hardware/drivers/ff552754(v=vs.85)">DestroyD3DBuffer</a>