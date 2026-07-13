---
UID: NS:ddkmapi._DDGETFIELDNUMOUT
title: DDGETFIELDNUMOUT (ddkmapi.h)
description: The DDGETFIELDNUMOUT structure contains the hardware video port's field number.
helpviewer_keywords: ["*LPDDGETFIELDNUMOUT","DDGETFIELDNUMOUT","DDGETFIELDNUMOUT structure [Display Devices]","LPDDGETFIELDNUMOUT","LPDDGETFIELDNUMOUT structure pointer [Display Devices]","ddkmapi/DDGETFIELDNUMOUT","ddkmapi/LPDDGETFIELDNUMOUT","ddstrcts_a52a121b-2050-41c3-a5ee-6ad474e3a666.xml","display.ddgetfieldnumout"]
old-location: display\ddgetfieldnumout.htm
tech.root: display
ms.assetid: 6af9d0be-03b7-4153-a4d6-cf36afe4fd0e
ms.date: 12/05/2018
ms.keywords: '*LPDDGETFIELDNUMOUT, DDGETFIELDNUMOUT, DDGETFIELDNUMOUT structure [Display Devices], LPDDGETFIELDNUMOUT, LPDDGETFIELDNUMOUT structure pointer [Display Devices], ddkmapi/DDGETFIELDNUMOUT, ddkmapi/LPDDGETFIELDNUMOUT, ddstrcts_a52a121b-2050-41c3-a5ee-6ad474e3a666.xml, display.ddgetfieldnumout'
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
req.typenames: DDGETFIELDNUMOUT, *LPDDGETFIELDNUMOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETFIELDNUMOUT
 - ddkmapi/_DDGETFIELDNUMOUT
 - LPDDGETFIELDNUMOUT
 - ddkmapi/LPDDGETFIELDNUMOUT
 - DDGETFIELDNUMOUT
 - ddkmapi/DDGETFIELDNUMOUT
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
 - DDGETFIELDNUMOUT
---

# DDGETFIELDNUMOUT structure


## -description

The DDGETFIELDNUMOUT structure contains the hardware video port's field number.

## -struct-fields

### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function for <a href="/previous-versions/windows/hardware/drivers/ff550686(v=vs.85)">DD_DXAPI_GET_VP_FIELD_NUMBER</a> operations. A return code of DD_OK indicates success.

### -field dwFieldNum

Specifies the hardware video port's field number.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550686(v=vs.85)">DD_DXAPI_GET_VP_FIELD_NUMBER</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>