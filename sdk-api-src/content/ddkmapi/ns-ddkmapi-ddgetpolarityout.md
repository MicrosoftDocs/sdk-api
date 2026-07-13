---
UID: NS:ddkmapi._DDGETPOLARITYOUT
title: DDGETPOLARITYOUT (ddkmapi.h)
description: The DDGETPOLARITYOUT structure contains the requested polarity information.
helpviewer_keywords: ["*LPDDGETPOLARITYOUT","DDGETPOLARITYOUT","DDGETPOLARITYOUT structure [Display Devices]","LPDDGETPOLARITYOUT","LPDDGETPOLARITYOUT structure pointer [Display Devices]","ddkmapi/DDGETPOLARITYOUT","ddkmapi/LPDDGETPOLARITYOUT","ddstrcts_fa20dcb8-4818-4c9d-8378-93c0fda09eff.xml","display.ddgetpolarityout"]
old-location: display\ddgetpolarityout.htm
tech.root: display
ms.assetid: f659ceff-39ba-4d74-98f2-ad12be730ffb
ms.date: 12/05/2018
ms.keywords: '*LPDDGETPOLARITYOUT, DDGETPOLARITYOUT, DDGETPOLARITYOUT structure [Display Devices], LPDDGETPOLARITYOUT, LPDDGETPOLARITYOUT structure pointer [Display Devices], ddkmapi/DDGETPOLARITYOUT, ddkmapi/LPDDGETPOLARITYOUT, ddstrcts_fa20dcb8-4818-4c9d-8378-93c0fda09eff.xml, display.ddgetpolarityout'
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
req.typenames: DDGETPOLARITYOUT, *LPDDGETPOLARITYOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETPOLARITYOUT
 - ddkmapi/_DDGETPOLARITYOUT
 - LPDDGETPOLARITYOUT
 - ddkmapi/LPDDGETPOLARITYOUT
 - DDGETPOLARITYOUT
 - ddkmapi/DDGETPOLARITYOUT
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
 - DDGETPOLARITYOUT
---

# DDGETPOLARITYOUT structure


## -description

The DDGETPOLARITYOUT structure contains the requested polarity information.

## -struct-fields

### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function for <a href="/previous-versions/windows/hardware/drivers/ff550660(v=vs.85)">DD_DXAPI_GET_POLARITY</a> operations. A return code of DD_OK indicates success.

### -field bPolarity

Specifies whether the field is an even or odd field of an interlaced video signal. A value of <b>TRUE</b> indicates even, <b>FALSE</b> indicates odd.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550660(v=vs.85)">DD_DXAPI_GET_POLARITY</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>