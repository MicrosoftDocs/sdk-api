---
UID: NC:ddrawint.PDD_VPORTCB_GETLINE
title: PDD_VPORTCB_GETLINE (ddrawint.h)
description: The DdVideoPortGetLine callback function returns the current line number of the hardware video port.
helpviewer_keywords: ["DdVideoPortGetLine","DdVideoPortGetLine callback function [Display Devices]","PDD_VPORTCB_GETLINE","PDD_VPORTCB_GETLINE callback","ddfncs_7695bbcc-355a-4934-bf3f-ad9a58607917.xml","ddrawint/DdVideoPortGetLine","display.ddvideoportgetline"]
old-location: display\ddvideoportgetline.htm
tech.root: display
ms.assetid: 6c0cfa87-bc16-47a6-8106-e5a1b1456813
ms.date: 12/05/2018
ms.keywords: DdVideoPortGetLine, DdVideoPortGetLine callback function [Display Devices], PDD_VPORTCB_GETLINE, PDD_VPORTCB_GETLINE callback, ddfncs_7695bbcc-355a-4934-bf3f-ad9a58607917.xml, ddrawint/DdVideoPortGetLine, display.ddvideoportgetline
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
 - PDD_VPORTCB_GETLINE
 - ddrawint/PDD_VPORTCB_GETLINE
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
 - DdVideoPortGetLine
---

## -description

The <b>DdVideoPortGetLine</b> callback function returns the current line number of the hardware video port.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportlinedata">DD_GETVPORTLINEDATA</a> structure that contains the information required for the driver to determine and return the current line number for the specified hardware video port.

## -returns

<b>DdVideoPortGetLine</b> returns one of the following callback codes:

## -remarks

Drivers that set the DDVPCAPS_READBACKLINE flag in the <b>dwCaps</b> member of the <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportcaps">DDVIDEOPORTCAPS</a> structure must implement <b>DdVideoPortGetLine</b>.

The driver should write the number of the current video line in the <b>dwLine</b> member of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportlinedata">DD_GETVPORTLINEDATA</a> structure at <i>lpGetLine</i>. The returned line number must be zero-based; that is, the first line of video is line 0, the second line of video is line 1, etc.

If the device is in a vertical blank, the driver should set DDERR_VERTICALBLANKINPROGRESS in the <b>ddRVal</b> member of <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportlinedata">DD_GETVPORTLINEDATA</a>. If the query cannot be performed because the hardware video port is disabled, the driver should set DDERR_VIDEONOTACTIVE in <b>ddRVal</b>. In both of these failed cases, the driver should return DDHAL_DRIVER_HANDLED.

## -see-also

<a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportcaps">DDVIDEOPORTCAPS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportlinedata">DD_GETVPORTLINEDATA</a>