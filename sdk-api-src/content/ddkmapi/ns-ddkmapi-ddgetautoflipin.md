---
UID: NS:ddkmapi._DDGETAUTOFLIPIN
title: DDGETAUTOFLIPIN (ddkmapi.h)
description: The DDGETAUTOFLIPIN structure contains the handle information.
helpviewer_keywords: ["*LPDDGETAUTOFLIPIN","DDGETAUTOFLIPIN","DDGETAUTOFLIPIN structure [Display Devices]","LPDDGETAUTOFLIPIN","LPDDGETAUTOFLIPIN structure pointer [Display Devices]","ddkmapi/DDGETAUTOFLIPIN","ddkmapi/LPDDGETAUTOFLIPIN","ddstrcts_7b504e9b-7380-42de-ac8f-ca7186a46354.xml","display.ddgetautoflipin"]
old-location: display\ddgetautoflipin.htm
tech.root: display
ms.assetid: aca9f7e4-3ec4-4575-9d2b-f2486ed50a53
ms.date: 12/05/2018
ms.keywords: '*LPDDGETAUTOFLIPIN, DDGETAUTOFLIPIN, DDGETAUTOFLIPIN structure [Display Devices], LPDDGETAUTOFLIPIN, LPDDGETAUTOFLIPIN structure pointer [Display Devices], ddkmapi/DDGETAUTOFLIPIN, ddkmapi/LPDDGETAUTOFLIPIN, ddstrcts_7b504e9b-7380-42de-ac8f-ca7186a46354.xml, display.ddgetautoflipin'
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
req.typenames: DDGETAUTOFLIPIN, *LPDDGETAUTOFLIPIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETAUTOFLIPIN
 - ddkmapi/_DDGETAUTOFLIPIN
 - LPDDGETAUTOFLIPIN
 - ddkmapi/LPDDGETAUTOFLIPIN
 - DDGETAUTOFLIPIN
 - ddkmapi/DDGETAUTOFLIPIN
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
 - DDGETAUTOFLIPIN
---

# DDGETAUTOFLIPIN structure


## -description

The DDGETAUTOFLIPIN structure contains the handle information.

## -struct-fields

### -field hDirectDraw

Specifies the Microsoft DirectDraw handle.

### -field hVideoPort

Specifies the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object handle.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550642(v=vs.85)">DD_DXAPI_GET_CURRENT_VP_AUTOFLIP_SURFACE</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>