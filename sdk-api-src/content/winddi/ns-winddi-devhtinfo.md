---
UID: NS:winddi._DEVHTINFO
title: DEVHTINFO (winddi.h)
description: The DEVHTINFO structure is used as input to the HTUI_DeviceColorAdjustment function.
helpviewer_keywords: ["*PDEVHTINFO","DEVHTINFO","DEVHTINFO structure [Display Devices]","PDEVHTINFO","PDEVHTINFO structure pointer [Display Devices]","display.devhtinfo","grstrcts_9ec57bb2-b77e-419b-8d26-03db8485cf35.xml","winddi/DEVHTINFO","winddi/PDEVHTINFO"]
old-location: display\devhtinfo.htm
tech.root: display
ms.assetid: 81abebbf-97f2-422f-b0ab-f6f920e09fef
ms.date: 12/05/2018
ms.keywords: '*PDEVHTINFO, DEVHTINFO, DEVHTINFO structure [Display Devices], PDEVHTINFO, PDEVHTINFO structure pointer [Display Devices], display.devhtinfo, grstrcts_9ec57bb2-b77e-419b-8d26-03db8485cf35.xml, winddi/DEVHTINFO, winddi/PDEVHTINFO'
req.header: winddi.h
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
req.typenames: DEVHTINFO, *PDEVHTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DEVHTINFO
 - winddi/_DEVHTINFO
 - PDEVHTINFO
 - winddi/PDEVHTINFO
 - DEVHTINFO
 - winddi/DEVHTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DEVHTINFO
---

# DEVHTINFO structure


## -description

The DEVHTINFO structure is used as input to the <a href="/windows/desktop/api/winddi/nf-winddi-htui_devicecoloradjustment">HTUI_DeviceColorAdjustment</a> function.

## -struct-fields

### -field HTFlags

Is a set of caller-supplied flags indicating halftone attributes. See the <b>flHTFlags</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a> structure for a complete list of possible values.

### -field HTPatternSize

Is a caller-supplied value that must be one of the HTPAT_SIZE-prefixed constants defined in <i>winddi.h</i>.

### -field DevPelsDPI

For printers, specifies the number of dots per inch. See the description of the <b>ulDevicePelsDPI</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a> structure for more information.

For displays, this member should be set to zero.

### -field ColorInfo

Is a caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-colorinfo">COLORINFO</a> structure containing halftoning color information.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-colorinfo">COLORINFO</a>



<a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-htui_devicecoloradjustment">HTUI_DeviceColorAdjustment</a>