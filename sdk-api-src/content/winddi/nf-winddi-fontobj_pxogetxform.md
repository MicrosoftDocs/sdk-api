---
UID: NF:winddi.FONTOBJ_pxoGetXform
title: FONTOBJ_pxoGetXform function (winddi.h)
description: The FONTOBJ_pxoGetXform function retrieves the notional-to-device transform for the specified font.
helpviewer_keywords: ["FONTOBJ_pxoGetXform","FONTOBJ_pxoGetXform function [Display Devices]","display.fontobj_pxogetxform","gdifncs_22900939-4aa1-4f8b-9345-1d74af8a7f71.xml","winddi/FONTOBJ_pxoGetXform"]
old-location: display\fontobj_pxogetxform.htm
tech.root: display
ms.assetid: 94d8ddf6-221f-47f0-8772-4364ad2ac1a2
ms.date: 12/05/2018
ms.keywords: FONTOBJ_pxoGetXform, FONTOBJ_pxoGetXform function [Display Devices], display.fontobj_pxogetxform, gdifncs_22900939-4aa1-4f8b-9345-1d74af8a7f71.xml, winddi/FONTOBJ_pxoGetXform
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FONTOBJ_pxoGetXform
 - winddi/FONTOBJ_pxoGetXform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - FONTOBJ_pxoGetXform
---

# FONTOBJ_pxoGetXform function


## -description

The <b>FONTOBJ_pxoGetXform</b> function retrieves the notional-to-device transform for the specified font.

## -parameters

### -param pfo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure for which the transform is to be retrieved.

## -returns

The return value is a pointer to an <a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a> structure that describes the transform. The XFORMOBJ structure can be used by the <b>XFORMOBJ_</b><b><i>Xxx</i></b> service routines. The XFORMOBJ structure assumes that: 

<ul>
<li>The distance between the pixels is in device space units. </li>
<li>Both notional and device space have positive values of y in the top-to-bottom direction. </li>
</ul>
If the font is a raster font, the return value is <b>NULL</b>.

## -remarks

The driver needs the notional-to-device transform to realize a driver-supplied font.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>



<a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a>