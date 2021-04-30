---
UID: NC:ddrawint.PDD_GETSCANLINE
title: PDD_GETSCANLINE (ddrawint.h)
description: The DdGetScanLine callback function returns the number of the current physical scan line.
helpviewer_keywords: ["DdGetScanLine","DdGetScanLine callback function [Display Devices]","PDD_GETSCANLINE","PDD_GETSCANLINE callback","ddfncs_640b22a3-e0aa-4e33-a510-36d91e5650cd.xml","ddrawint/DdGetScanLine","display.ddgetscanline"]
old-location: display\ddgetscanline.htm
tech.root: display
ms.assetid: 3738205f-2d27-4211-944a-6ca71954fe47
ms.date: 12/05/2018
ms.keywords: DdGetScanLine, DdGetScanLine callback function [Display Devices], PDD_GETSCANLINE, PDD_GETSCANLINE callback, ddfncs_640b22a3-e0aa-4e33-a510-36d91e5650cd.xml, ddrawint/DdGetScanLine, display.ddgetscanline
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDD_GETSCANLINE
 - ddrawint/PDD_GETSCANLINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdGetScanLine
---




## -description

The <i>DdGetScanLine</i> callback function returns the number of the current physical scan line.

## -parameters

### -param unnamedParam1


Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getscanlinedata">DD_GETSCANLINEDATA</a> structure in which the driver returns the number of the current scan line.

## -returns

<i>DdGetScanLine</i> returns one of the following callback codes:

## -remarks

If the monitor is not in vertical blank, the driver should write the scan line value in the <b>dwScanLine</b> member of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getscanlinedata">DD_GETSCANLINEDATA</a> structure at <i>pGetScanLine</i>. The number must be in the range [0, <i>n</i>], where scan line 0 is the first visible scan line and scan line <i>n</i> is the last visible scan line on the screen. The driver should then set DD_OK in the <b>ddRVal</b> member of <b>DD_GETSCANLINEDATA</b> and return DDHAL_DRIVER_HANDLED.

The scan line is indeterminate if a vertical blank is in progress. In this situation, the driver should set <b>ddRVal</b> to DDERR_VERTICALBLANKINPROGRESS and return DDHAL_DRIVER_HANDLED.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getscanlinedata">DD_GETSCANLINEDATA</a>