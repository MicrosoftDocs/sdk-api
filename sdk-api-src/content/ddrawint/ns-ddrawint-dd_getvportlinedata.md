---
UID: NS:ddrawint._DD_GETVPORTLINEDATA
title: DD_GETVPORTLINEDATA (ddrawint.h)
description: The DD_GETVPORTLINEDATA structure contains the current line number of the hardware video port.
helpviewer_keywords: ["*PDD_GETVPORTLINEDATA","DD_GETVPORTLINEDATA","DD_GETVPORTLINEDATA structure [Display Devices]","ddrawint/DD_GETVPORTLINEDATA","ddstrcts_81a8dc13-0681-4135-a74a-f7aa22408156.xml","display.dd_getvportlinedata"]
old-location: display\dd_getvportlinedata.htm
tech.root: display
ms.assetid: d8b2803c-38be-40ea-b46b-4bab1ce55534
ms.date: 12/05/2018
ms.keywords: '*PDD_GETVPORTLINEDATA, DD_GETVPORTLINEDATA, DD_GETVPORTLINEDATA structure [Display Devices], ddrawint/DD_GETVPORTLINEDATA, ddstrcts_81a8dc13-0681-4135-a74a-f7aa22408156.xml, display.dd_getvportlinedata'
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
req.typenames: '*PDD_GETVPORTLINEDATA, DD_GETVPORTLINEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETVPORTLINEDATA
 - ddrawint/_DD_GETVPORTLINEDATA
 - PDD_GETVPORTLINEDATA
 - ddrawint/PDD_GETVPORTLINEDATA
 - DD_GETVPORTLINEDATA
 - ddrawint/DD_GETVPORTLINEDATA
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
 - DD_GETVPORTLINEDATA
---

# DD_GETVPORTLINEDATA structure


## -description

The DD_GETVPORTLINEDATA structure contains the current line number of the hardware video port.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpVideoPort

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents this <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

### -field dwLine

Specifies the location in which the driver should write the current line number on the hardware video port.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getline">DdVideoPortGetLine</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetVideoPortLine

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getline">DdVideoPortGetLine</a>