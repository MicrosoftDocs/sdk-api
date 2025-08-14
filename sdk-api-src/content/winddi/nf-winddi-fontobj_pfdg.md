---
UID: NF:winddi.FONTOBJ_pfdg
title: FONTOBJ_pfdg function (winddi.h)
description: The FONTOBJ_pfdg function retrieves the pointer to the FD_GLYPHSET structure associated with the specified font.
helpviewer_keywords: ["FONTOBJ_pfdg","FONTOBJ_pfdg function [Display Devices]","display.fontobj_pfdg","gdifncs_858ebe0b-c792-4472-967d-cdf46ec12c28.xml","winddi/FONTOBJ_pfdg"]
old-location: display\fontobj_pfdg.htm
tech.root: display
ms.assetid: 5813b06e-5fa8-4279-bd16-aa7b7129a181
ms.date: 12/05/2018
ms.keywords: FONTOBJ_pfdg, FONTOBJ_pfdg function [Display Devices], display.fontobj_pfdg, gdifncs_858ebe0b-c792-4472-967d-cdf46ec12c28.xml, winddi/FONTOBJ_pfdg
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
 - FONTOBJ_pfdg
 - winddi/FONTOBJ_pfdg
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
 - FONTOBJ_pfdg
---

# FONTOBJ_pfdg function


## -description

The <b>FONTOBJ_pfdg</b> function retrieves the pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-fd_glyphset">FD_GLYPHSET</a> structure associated with the specified font.

## -parameters

### -param pfo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure for which the associated FD_GLYPHSET structure is to be returned.

## -returns

<b>FONTOBJ_pfdg</b> returns a pointer to the FD_GLYPHSET structure associated with the specified font.

## -remarks

Printer drivers can call <b>FONTOBJ_pfdg</b> to determine which Unicode code points are supported in a GDI font. The printer driver can then determine whether it can optimize performance by instead using a similar printer-resident font to display a text string.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-fd_glyphset">FD_GLYPHSET</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>