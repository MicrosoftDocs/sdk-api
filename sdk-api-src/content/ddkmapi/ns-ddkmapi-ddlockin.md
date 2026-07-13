---
UID: NS:ddkmapi._DDLOCKIN
title: DDLOCKIN (ddkmapi.h)
description: The DDLOCKIN structure contains the Microsoft DirectDraw object and DirectDraw surface handle information.
helpviewer_keywords: ["*LPDDLOCKIN","DDLOCKIN","DDLOCKIN structure [Display Devices]","LPDDLOCKIN","LPDDLOCKIN structure pointer [Display Devices]","ddkmapi/DDLOCKIN","ddkmapi/LPDDLOCKIN","ddstrcts_b8a5f627-94dd-4353-b9f1-edc6f65adaba.xml","display.ddlockin"]
old-location: display\ddlockin.htm
tech.root: display
ms.assetid: 47bc1879-80a5-4850-a303-dbbebbd83de6
ms.date: 12/05/2018
ms.keywords: '*LPDDLOCKIN, DDLOCKIN, DDLOCKIN structure [Display Devices], LPDDLOCKIN, LPDDLOCKIN structure pointer [Display Devices], ddkmapi/DDLOCKIN, ddkmapi/LPDDLOCKIN, ddstrcts_b8a5f627-94dd-4353-b9f1-edc6f65adaba.xml, display.ddlockin'
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
req.typenames: DDLOCKIN, *LPDDLOCKIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDLOCKIN
 - ddkmapi/_DDLOCKIN
 - LPDDLOCKIN
 - ddkmapi/LPDDLOCKIN
 - DDLOCKIN
 - ddkmapi/DDLOCKIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDLOCKIN
---

# DDLOCKIN structure


## -description

The DDLOCKIN structure contains the Microsoft DirectDraw object and DirectDraw surface handle information.

## -struct-fields

### -field hDirectDraw

Specifies the DirectDraw handle.

### -field hSurface

Specifies the DirectDrawSurface handle.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550695(v=vs.85)">DD_DXAPI_LOCK</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>