---
UID: NS:ddkmapi._DDCAPBUFFINFO
title: DDCAPBUFFINFO (ddkmapi.h)
description: The DDCAPBUFFINFO structure contains the capture information.
helpviewer_keywords: ["*LPDDCAPBUFFINFO","DDCAPBUFFINFO","DDCAPBUFFINFO structure [Display Devices]","LPDDCAPBUFFINFO","LPDDCAPBUFFINFO structure pointer [Display Devices]","ddkmapi/DDCAPBUFFINFO","ddkmapi/LPDDCAPBUFFINFO","ddstrcts_c1b7049e-f505-419f-ba3e-53625521dae2.xml","display.ddcapbuffinfo"]
old-location: display\ddcapbuffinfo.htm
tech.root: display
ms.assetid: 8286c433-2183-4751-be8a-30cb9cd9146d
ms.date: 12/05/2018
ms.keywords: '*LPDDCAPBUFFINFO, DDCAPBUFFINFO, DDCAPBUFFINFO structure [Display Devices], LPDDCAPBUFFINFO, LPDDCAPBUFFINFO structure pointer [Display Devices], ddkmapi/DDCAPBUFFINFO, ddkmapi/LPDDCAPBUFFINFO, ddstrcts_c1b7049e-f505-419f-ba3e-53625521dae2.xml, display.ddcapbuffinfo'
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
req.typenames: DDCAPBUFFINFO, *LPDDCAPBUFFINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDCAPBUFFINFO
 - ddkmapi/_DDCAPBUFFINFO
 - LPDDCAPBUFFINFO
 - ddkmapi/LPDDCAPBUFFINFO
 - DDCAPBUFFINFO
 - ddkmapi/DDCAPBUFFINFO
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
 - DDCAPBUFFINFO
---

# DDCAPBUFFINFO structure


## -description

The DDCAPBUFFINFO structure contains the capture information.

## -struct-fields

### -field dwFieldNumber

Indicates the internal field number of the field captured.

### -field bPolarity

Specifies whether the captured field is an even or odd field. A value of 0x00000001 indicates even, 0x00000000 indicates odd.

### -field liTimeStamp

Used by Microsoft DirectDraw and should be ignored by the driver.

### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function for the <a href="/previous-versions/windows/hardware/drivers/ff550599(v=vs.85)">DD_DXAPI_ADDVPCAPTUREBUFFER</a> operation. Contains DD_OK if the capture buffer contains valid data.

## -see-also

<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddaddvpcapturebuff">DDADDVPCAPTUREBUFF</a>



<a href="/previous-versions/windows/hardware/drivers/ff550599(v=vs.85)">DD_DXAPI_ADDVPCAPTUREBUFFER</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>