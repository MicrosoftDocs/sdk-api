---
UID: NS:ddrawint._DD_GETSCANLINEDATA
title: DD_GETSCANLINEDATA (ddrawint.h)
description: The DD_GETSCANLINEDATA structure contains the members required to query and return the number of the current scan line.
helpviewer_keywords: ["*PDD_GETSCANLINEDATA","DD_GETSCANLINEDATA","DD_GETSCANLINEDATA structure [Display Devices]","ddrawint/DD_GETSCANLINEDATA","ddstrcts_f7654548-917a-4c6d-a15a-0f09bca64b5d.xml","display.dd_getscanlinedata"]
old-location: display\dd_getscanlinedata.htm
tech.root: display
ms.assetid: 92433daa-43da-40d3-a319-e0d70abd3cb0
ms.date: 12/05/2018
ms.keywords: '*PDD_GETSCANLINEDATA, DD_GETSCANLINEDATA, DD_GETSCANLINEDATA structure [Display Devices], ddrawint/DD_GETSCANLINEDATA, ddstrcts_f7654548-917a-4c6d-a15a-0f09bca64b5d.xml, display.dd_getscanlinedata'
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
req.typenames: '*PDD_GETSCANLINEDATA, DD_GETSCANLINEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETSCANLINEDATA
 - ddrawint/_DD_GETSCANLINEDATA
 - PDD_GETSCANLINEDATA
 - ddrawint/PDD_GETSCANLINEDATA
 - DD_GETSCANLINEDATA
 - ddrawint/DD_GETSCANLINEDATA
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
 - DD_GETSCANLINEDATA
---

# DD_GETSCANLINEDATA structure


## -description

The DD_GETSCANLINEDATA structure contains the members required to query and return the number of the current scan line.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field dwScanLine

Specifies the location in which the driver returns the number of the current scan line. See the Remarks section for more information.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getscanline">DdGetScanLine</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetScanLine

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

## -remarks

The returned scan line value in <b>dwScanLine</b> must be greater than or equal to 0 and less than N, where N is the sum of the number of visible scan lines and the number of scan lines that occur during vertical blank. For example, with a display operating at a resolution of 640x480, that has 12 scan lines during vertical blank, the value returned to <b>GetScanLine</b> could range from 0 to 491.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getscanline">DdGetScanLine</a>