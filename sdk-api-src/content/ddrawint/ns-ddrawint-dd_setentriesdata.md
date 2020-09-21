---
UID: NS:ddrawint._DD_SETENTRIESDATA
title: DD_SETENTRIESDATA (ddrawint.h)
description: The DD_SETENTRIESDATA structure contains information necessary to set palette entries.
helpviewer_keywords: ["*PDD_SETENTRIESDATA","DD_SETENTRIESDATA","DD_SETENTRIESDATA structure [Display Devices]","ddrawint/DD_SETENTRIESDATA","ddstrcts_dc575bf2-1249-4d66-aba9-aba1856358df.xml","display.dd_setentriesdata"]
old-location: display\dd_setentriesdata.htm
tech.root: display
ms.assetid: 9420f41a-401b-4fc3-b9a4-f2bfe6cb2710
ms.date: 12/05/2018
ms.keywords: '*PDD_SETENTRIESDATA, DD_SETENTRIESDATA, DD_SETENTRIESDATA structure [Display Devices], ddrawint/DD_SETENTRIESDATA, ddstrcts_dc575bf2-1249-4d66-aba9-aba1856358df.xml, display.dd_setentriesdata'
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
req.typenames: '*PDD_SETENTRIESDATA, DD_SETENTRIESDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_SETENTRIESDATA
 - ddrawint/_DD_SETENTRIESDATA
 - PDD_SETENTRIESDATA
 - ddrawint/PDD_SETENTRIESDATA
 - DD_SETENTRIESDATA
 - ddrawint/DD_SETENTRIESDATA
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
 - DD_SETENTRIESDATA
---

# DD_SETENTRIESDATA structure


## -description

The DD_SETENTRIESDATA structure contains information necessary to set palette entries.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDPalette

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palette_global">DD_PALETTE_GLOBAL</a> structure that represents the DirectDrawPalette object.

### -field dwBase

Specifies a zero-based index into the color table of the first entry to be modified.

### -field dwNumEntries

Specifies the number of palette entries that the driver should update.

### -field lpEntries

Points to a PALETTEENTRY structure that specifies the color table. See the latest Microsoft DirectX SDK documentation for more information about PALETTEENTRY.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_palcb_setentries">DdSetEntries</a> callback. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field SetEntries

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_palcb_setentries">DdSetEntries</a>