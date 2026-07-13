---
UID: NS:ddkmapi._DDGETPOLARITYIN
title: DDGETPOLARITYIN (ddkmapi.h)
description: The DDGETPOLARITYIN structure contains the Microsoft DirectDraw and video port extensions (VPE) object handles.
helpviewer_keywords: ["*LPDDGETPOLARITYIN","DDGETPOLARITYIN","DDGETPOLARITYIN structure [Display Devices]","LPDDGETPOLARITYIN","LPDDGETPOLARITYIN structure pointer [Display Devices]","ddkmapi/DDGETPOLARITYIN","ddkmapi/LPDDGETPOLARITYIN","ddstrcts_d84baddb-b5f0-4b66-86fd-504dbf05608c.xml","display.ddgetpolarityin"]
old-location: display\ddgetpolarityin.htm
tech.root: display
ms.assetid: 8ef7a1b7-1111-440d-8318-46d2135142e2
ms.date: 12/05/2018
ms.keywords: '*LPDDGETPOLARITYIN, DDGETPOLARITYIN, DDGETPOLARITYIN structure [Display Devices], LPDDGETPOLARITYIN, LPDDGETPOLARITYIN structure pointer [Display Devices], ddkmapi/DDGETPOLARITYIN, ddkmapi/LPDDGETPOLARITYIN, ddstrcts_d84baddb-b5f0-4b66-86fd-504dbf05608c.xml, display.ddgetpolarityin'
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
req.typenames: DDGETPOLARITYIN, *LPDDGETPOLARITYIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETPOLARITYIN
 - ddkmapi/_DDGETPOLARITYIN
 - LPDDGETPOLARITYIN
 - ddkmapi/LPDDGETPOLARITYIN
 - DDGETPOLARITYIN
 - ddkmapi/DDGETPOLARITYIN
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
 - DDGETPOLARITYIN
---

# DDGETPOLARITYIN structure


## -description

The DDGETPOLARITYIN structure contains the Microsoft DirectDraw and <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object handles.

## -struct-fields

### -field hDirectDraw

Specifies the DirectDraw handle.

### -field hVideoPort

Specifies the VPE object handle.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550660(v=vs.85)">DD_DXAPI_GET_POLARITY</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>