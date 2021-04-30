---
UID: NC:ddrawint.PDD_PALCB_DESTROYPALETTE
title: PDD_PALCB_DESTROYPALETTE (ddrawint.h)
description: The DdDestroyPalette callback function destroys the specified palette.
helpviewer_keywords: ["DdDestroyPalette","DdDestroyPalette callback function [Display Devices]","PDD_PALCB_DESTROYPALETTE","PDD_PALCB_DESTROYPALETTE callback","ddfncs_a0c991ff-d3b8-4793-a6b3-a72dc5f5d700.xml","ddrawint/DdDestroyPalette","display.dddestroypalette"]
old-location: display\dddestroypalette.htm
tech.root: display
ms.assetid: b44936fd-0052-4f54-9e97-1664c381c697
ms.date: 12/05/2018
ms.keywords: DdDestroyPalette, DdDestroyPalette callback function [Display Devices], PDD_PALCB_DESTROYPALETTE, PDD_PALCB_DESTROYPALETTE callback, ddfncs_a0c991ff-d3b8-4793-a6b3-a72dc5f5d700.xml, ddrawint/DdDestroyPalette, display.dddestroypalette
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
 - PDD_PALCB_DESTROYPALETTE
 - ddrawint/PDD_PALCB_DESTROYPALETTE
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
 - DdDestroyPalette
---

## -description

The <b>DdDestroyPalette</b> callback function destroys the specified palette.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_destroypalettedata">DD_DESTROYPALETTEDATA</a> structure that contains the information needed to destroy a palette.

## -returns

<b>DdDestroyPalette</b> returns one of the following callback codes:

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_destroypalettedata">DD_DESTROYPALETTEDATA</a>