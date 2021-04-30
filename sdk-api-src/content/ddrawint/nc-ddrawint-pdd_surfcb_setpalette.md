---
UID: NC:ddrawint.PDD_SURFCB_SETPALETTE
title: PDD_SURFCB_SETPALETTE (ddrawint.h)
description: The DdSetPalette callback function attaches a palette to the specified surface.
helpviewer_keywords: ["DdSetPalette","DdSetPalette callback function [Display Devices]","PDD_SURFCB_SETPALETTE","PDD_SURFCB_SETPALETTE callback","ddfncs_7d4146b2-d5f8-4a02-b24e-3dfa0a8d817a.xml","ddrawint/DdSetPalette","display.ddsetpalette"]
old-location: display\ddsetpalette.htm
tech.root: display
ms.assetid: 745b30f0-3d2f-4894-8991-6b7d511f8493
ms.date: 12/05/2018
ms.keywords: DdSetPalette, DdSetPalette callback function [Display Devices], PDD_SURFCB_SETPALETTE, PDD_SURFCB_SETPALETTE callback, ddfncs_7d4146b2-d5f8-4a02-b24e-3dfa0a8d817a.xml, ddrawint/DdSetPalette, display.ddsetpalette
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
 - PDD_SURFCB_SETPALETTE
 - ddrawint/PDD_SURFCB_SETPALETTE
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
 - DdSetPalette
---

## -description

The <b>DdSetPalette</b> callback function attaches a palette to the specified surface.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_setpalettedata">DD_SETPALETTEDATA</a> structure that contains the information required to set a palette to the specified surface.

## -returns

<b>DdSetPalette</b> returns one of the following callback codes:

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_setpalettedata">DD_SETPALETTEDATA</a>