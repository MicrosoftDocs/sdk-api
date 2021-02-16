---
UID: NS:ddrawint._DD_GETMOCOMPCOMPBUFFDATA
title: DD_GETMOCOMPCOMPBUFFDATA (ddrawint.h)
description: The DD_GETMOCOMPCOMPBUFFDATA structure contains the compressed buffer information.
helpviewer_keywords: ["*PDD_GETMOCOMPCOMPBUFFDATA","DD_GETMOCOMPCOMPBUFFDATA","DD_GETMOCOMPCOMPBUFFDATA structure [Display Devices]","ddrawint/DD_GETMOCOMPCOMPBUFFDATA","ddstrcts_20d1802e-7979-4336-b730-a161f771c24a.xml","display.dd_getmocompcompbuffdata"]
old-location: display\dd_getmocompcompbuffdata.htm
tech.root: display
ms.assetid: 5510d430-834c-42ea-a113-c17b1b87ea52
ms.date: 12/05/2018
ms.keywords: '*PDD_GETMOCOMPCOMPBUFFDATA, DD_GETMOCOMPCOMPBUFFDATA, DD_GETMOCOMPCOMPBUFFDATA structure [Display Devices], ddrawint/DD_GETMOCOMPCOMPBUFFDATA, ddstrcts_20d1802e-7979-4336-b730-a161f771c24a.xml, display.dd_getmocompcompbuffdata'
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
req.typenames: '*PDD_GETMOCOMPCOMPBUFFDATA, DD_GETMOCOMPCOMPBUFFDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETMOCOMPCOMPBUFFDATA
 - ddrawint/_DD_GETMOCOMPCOMPBUFFDATA
 - PDD_GETMOCOMPCOMPBUFFDATA
 - ddrawint/PDD_GETMOCOMPCOMPBUFFDATA
 - DD_GETMOCOMPCOMPBUFFDATA
 - ddrawint/DD_GETMOCOMPCOMPBUFFDATA
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
 - DD_GETMOCOMPCOMPBUFFDATA
---

# DD_GETMOCOMPCOMPBUFFDATA structure


## -description

The DD_GETMOCOMPCOMPBUFFDATA structure contains the compressed buffer information.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpGuid

Points to a GUID for which the compressed buffer information is requested.

### -field dwWidth

Indicates the width in pixels of the uncompressed output frame.

### -field dwHeight

Indicates the height in pixels of the uncompressed output frame.

### -field ddPixelFormat

Points to a <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure that contains the pixel format of the uncompressed output frame.

### -field dwNumTypesCompBuffs

Indicates how many different types of surfaces the driver requires to perform motion compensation using the requested GUID.

### -field lpCompBuffInfo

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-ddcompbufferinfo">DDCOMPBUFFERINFO</a> structure that contains the driver-supplied information for each type of required surface.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getcompbuffinfo">DdMoCompGetBuffInfo</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getcompbuffinfo">DdMoCompGetBuffInfo</a>