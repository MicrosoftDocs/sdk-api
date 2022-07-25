---
UID: NC:ddrawint.PDD_SURFCB_BLT
title: PDD_SURFCB_BLT (ddrawint.h)
description: The DdBlt callback function performs a bit-block transfer.
helpviewer_keywords: ["DdBlt","DdBlt callback function [Display Devices]","PDD_SURFCB_BLT","PDD_SURFCB_BLT callback","ddfncs_464b3f37-739d-45c9-955d-3103c6a21047.xml","ddrawint/DdBlt","display.ddblt"]
old-location: display\ddblt.htm
tech.root: display
ms.assetid: 28e0c827-33f1-4b83-9f20-bbb66bc0e14a
ms.date: 12/05/2018
ms.keywords: DdBlt, DdBlt callback function [Display Devices], PDD_SURFCB_BLT, PDD_SURFCB_BLT callback, ddfncs_464b3f37-739d-45c9-955d-3103c6a21047.xml, ddrawint/DdBlt, display.ddblt
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
 - PDD_SURFCB_BLT
 - ddrawint/PDD_SURFCB_BLT
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
 - DdBlt
---

## -description

The <i>DdBlt</i> callback function performs a bit-block transfer.

## -parameters

### -param unnamedParam1

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_bltdata">DD_BLTDATA</a> structure that contains the information required for the driver to perform the blit.

## -returns

<i>DdBlt</i> returns one of the following callback codes:

## -remarks

<i>DdBlt</i> can be optionally implemented in DirectDraw drivers.

Before performing the bit block transfer, the driver should ensure that a flip involving the destination surface is not in progress. If the destination surface is involved in a flip, the driver should set the <b>ddRVal</b> member of the DD_BLTDATA structure at <i>lpBlt</i> to DDERR_WASSTILLDRAWING and return DDHAL_DRIVER_HANDLED.

The driver should check <b>dwFlags</b> to determine the type of blit operation to perform. The driver should not check for flags that are undocumented.

When performing transparent (color keyed) blts, drivers should ignore any unused pixel bits in their comparisons. (For instance in 32bpp modes, the high byte is typically unused. This byte should not be used in the color key comparison.)

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_bltdata">DD_BLTDATA</a>