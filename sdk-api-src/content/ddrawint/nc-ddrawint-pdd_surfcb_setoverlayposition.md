---
UID: NC:ddrawint.PDD_SURFCB_SETOVERLAYPOSITION
title: PDD_SURFCB_SETOVERLAYPOSITION (ddrawint.h)
description: The DdSetOverlayPosition callback function sets the position for an overlay.
helpviewer_keywords: ["DdSetOverlayPosition","DdSetOverlayPosition callback function [Display Devices]","PDD_SURFCB_SETOVERLAYPOSITION","PDD_SURFCB_SETOVERLAYPOSITION callback","ddfncs_9e5f3748-1da5-4512-9024-88939ee0d3fc.xml","ddrawint/DdSetOverlayPosition","display.ddsetoverlayposition"]
old-location: display\ddsetoverlayposition.htm
tech.root: display
ms.assetid: 0bafdeea-d06d-4c25-9ee5-b7df23d7dd20
ms.date: 12/05/2018
ms.keywords: DdSetOverlayPosition, DdSetOverlayPosition callback function [Display Devices], PDD_SURFCB_SETOVERLAYPOSITION, PDD_SURFCB_SETOVERLAYPOSITION callback, ddfncs_9e5f3748-1da5-4512-9024-88939ee0d3fc.xml, ddrawint/DdSetOverlayPosition, display.ddsetoverlayposition
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
 - PDD_SURFCB_SETOVERLAYPOSITION
 - ddrawint/PDD_SURFCB_SETOVERLAYPOSITION
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
 - DdSetOverlayPosition
---

## -description

The <b>DdSetOverlayPosition</b> callback function sets the position for an overlay.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata">DD_SETOVERLAYPOSITIONDATA</a> structure that contains the information required to set the overlay position.

## -returns

<b>DdSetOverlayPosition</b> returns one of the following callback codes:

## -remarks

When the overlay is visible, the driver should cause the overlay to be displayed on the primary surface. The upper left corner of the overlay should be anchored at the position specified by the <b>lXPos</b> and <b>lYPos</b> members of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata">DD_SETOVERLAYPOSITIONDATA</a> structure at <i>lpSetOverlayPosition</i>. For example, values of (0,0) indicate that the upper left corner of the overlay should appear in the upper left corner of the surface identified by the <b>lpDDDestSurface</b> member of DD_SETOVERLAYPOSITIONDATA.

When the overlay is invisible, the driver should set an error code in the <b>ddRVal</b> member of DD_SETOVERLAYPOSITIONDATA and return DDHAL_DRIVER_HANDLED.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata">DD_SETOVERLAYPOSITIONDATA</a>