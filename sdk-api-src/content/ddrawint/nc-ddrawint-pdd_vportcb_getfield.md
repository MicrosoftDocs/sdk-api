---
UID: NC:ddrawint.PDD_VPORTCB_GETFIELD
title: PDD_VPORTCB_GETFIELD (ddrawint.h)
description: The DdVideoPortGetField callback function determines whether the current field of an interlaced signal is even or odd.
helpviewer_keywords: ["DdVideoPortGetField","DdVideoPortGetField callback function [Display Devices]","PDD_VPORTCB_GETFIELD","PDD_VPORTCB_GETFIELD callback","ddfncs_85abec9a-0917-4bde-88c7-9d94ead1745c.xml","ddrawint/DdVideoPortGetField","display.ddvideoportgetfield"]
old-location: display\ddvideoportgetfield.htm
tech.root: display
ms.assetid: e8c99103-31cd-4468-8b6b-1e56b31e10da
ms.date: 12/05/2018
ms.keywords: DdVideoPortGetField, DdVideoPortGetField callback function [Display Devices], PDD_VPORTCB_GETFIELD, PDD_VPORTCB_GETFIELD callback, ddfncs_85abec9a-0917-4bde-88c7-9d94ead1745c.xml, ddrawint/DdVideoPortGetField, display.ddvideoportgetfield
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
 - PDD_VPORTCB_GETFIELD
 - ddrawint/PDD_VPORTCB_GETFIELD
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
 - DdVideoPortGetField
---

## -description

The <b>DdVideoPortGetField</b> callback function determines whether the current field of an interlaced signal is even or odd.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportfielddata">DD_GETVPORTFIELDDATA</a> structure that contains the information required for the driver to determine whether the current field is even or odd.

## -returns

<b>DdVideoPortGetField</b> returns one of the following callback codes:

## -remarks

DirectDraw drivers that set the DDVPCAPS_READBACKFIELD flag in the <b>dwCaps</b> member of the <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportcaps">DDVIDEOPORTCAPS</a> structure must implement <b>DdVideoPortGetField</b>.

The driver should determine whether the current field is even or odd and write <b>TRUE</b> or <b>FALSE</b> in the <b>bField</b> member of the DD_GETVPORTFIELDDATA structure at <b>lpGetField</b>, accordingly. If the query cannot be performed because the hardware video port is disabled, the driver should return DDHAL_DRIVER_HANDLED and set DDERR_VIDEONOTACTIVE in the <b>ddRVal</b> member of DD_GETVPORTFIELDDATA.

## -see-also

<a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportcaps">DDVIDEOPORTCAPS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportfielddata">DD_GETVPORTFIELDDATA</a>