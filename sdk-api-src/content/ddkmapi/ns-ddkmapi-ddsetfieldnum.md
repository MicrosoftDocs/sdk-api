---
UID: NS:ddkmapi._DDSETFIELDNUM
title: DDSETFIELDNUM (ddkmapi.h)
description: The DDSETFIELDNUM structure contains the handles and the field number.
helpviewer_keywords: ["*LPDDSETFIELDNUM","DDSETFIELDNUM","DDSETFIELDNUM structure [Display Devices]","LPDDSETFIELDNUM","LPDDSETFIELDNUM structure pointer [Display Devices]","ddkmapi/DDSETFIELDNUM","ddkmapi/LPDDSETFIELDNUM","ddstrcts_d8753497-b27b-4bd5-adcd-5b76e2169535.xml","display.ddsetfieldnum"]
old-location: display\ddsetfieldnum.htm
tech.root: display
ms.assetid: 442a4bbf-e3d9-4b06-99c4-1ffcf708a15c
ms.date: 12/05/2018
ms.keywords: '*LPDDSETFIELDNUM, DDSETFIELDNUM, DDSETFIELDNUM structure [Display Devices], LPDDSETFIELDNUM, LPDDSETFIELDNUM structure pointer [Display Devices], ddkmapi/DDSETFIELDNUM, ddkmapi/LPDDSETFIELDNUM, ddstrcts_d8753497-b27b-4bd5-adcd-5b76e2169535.xml, display.ddsetfieldnum'
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
req.typenames: DDSETFIELDNUM, *LPDDSETFIELDNUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDSETFIELDNUM
 - ddkmapi/_DDSETFIELDNUM
 - LPDDSETFIELDNUM
 - ddkmapi/LPDDSETFIELDNUM
 - DDSETFIELDNUM
 - ddkmapi/DDSETFIELDNUM
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
 - DDSETFIELDNUM
---

# DDSETFIELDNUM structure


## -description

The DDSETFIELDNUM structure contains the handles and the field number.

## -struct-fields

### -field hDirectDraw

Specifies the Microsoft DirectDraw handle.

### -field hVideoPort

Specifies the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object handle.

### -field dwFieldNum

Specifies the hardware video port's field number to be set.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff551507(v=vs.85)">DD_DXAPI_SET_VP_FIELD_NUMBER</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>