---
UID: NC:ddrawint.PDD_CREATEPALETTE
title: PDD_CREATEPALETTE (ddrawint.h)
description: The DdCreatePalette callback function creates a DirectDrawPalette object for the specified DirectDraw object.
helpviewer_keywords: ["DdCreatePalette","DdCreatePalette callback function [Display Devices]","PDD_CREATEPALETTE","PDD_CREATEPALETTE callback","ddfncs_5930e0e6-1029-4c6d-aa6b-b8050e2f9d9d.xml","ddrawint/DdCreatePalette","display.ddcreatepalette"]
old-location: display\ddcreatepalette.htm
tech.root: display
ms.assetid: 047d63c6-eb4c-4944-8c98-0f9686e2c37a
ms.date: 12/05/2018
ms.keywords: DdCreatePalette, DdCreatePalette callback function [Display Devices], PDD_CREATEPALETTE, PDD_CREATEPALETTE callback, ddfncs_5930e0e6-1029-4c6d-aa6b-b8050e2f9d9d.xml, ddrawint/DdCreatePalette, display.ddcreatepalette
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
 - PDD_CREATEPALETTE
 - ddrawint/PDD_CREATEPALETTE
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
 - DdCreatePalette
---

## -description

The <b>DdCreatePalette</b> callback function creates a DirectDrawPalette object for the specified DirectDraw object.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_createpalettedata">DD_CREATEPALETTEDATA</a> structure that contains the information necessary to create the DirectDrawPalette object.

## -returns

<b>DdCreatePalette</b> returns one of the following callback codes:

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_createpalettedata">DD_CREATEPALETTEDATA</a>