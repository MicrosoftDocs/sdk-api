---
UID: NC:ddrawint.PDD_SURFCB_FLIP
title: PDD_SURFCB_FLIP (ddrawint.h)
description: The DdFlip callback function causes the surface memory associated with the target surface to become the primary surface, and the current surface to become the nonprimary surface.
helpviewer_keywords: ["DdFlip","DdFlip callback function [Display Devices]","PDD_SURFCB_FLIP","PDD_SURFCB_FLIP callback","ddfncs_c7f9b1ea-0c9e-47f3-8fd1-b814d6e6adbd.xml","ddrawint/DdFlip","display.ddflip"]
old-location: display\ddflip.htm
tech.root: display
ms.assetid: 4ce2e967-7b4a-4065-844d-d8852dec8a8f
ms.date: 12/05/2018
ms.keywords: DdFlip, DdFlip callback function [Display Devices], PDD_SURFCB_FLIP, PDD_SURFCB_FLIP callback, ddfncs_c7f9b1ea-0c9e-47f3-8fd1-b814d6e6adbd.xml, ddrawint/DdFlip, display.ddflip
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
 - PDD_SURFCB_FLIP
 - ddrawint/PDD_SURFCB_FLIP
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
 - DdFlip
---

## -description

The <b>DdFlip</b> callback function causes the surface memory associated with the target surface to become the primary surface, and the current surface to become the nonprimary surface.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_flipdata">DD_FLIPDATA</a> structure that contains the information required to perform the flip.

## -returns

<b>DdFlip</b> returns one of the following callback codes:

## -remarks

<b>DdFlip</b> allows a display driver to perform multibuffering. DirectDraw drivers must implement this function.

The driver should update its surface pointers so that the next frame will be written to the surface to which the <b>lpSurfTarg</b> member of the DD_FLIPDATA structure at <b>lpFlip</b> points. If a previous flip request is still pending, the driver should fail the call by setting the <b>ddRVal</b> member of DD_FLIPDATA to DDERR_WASSTILLDRAWING and returning DDHAL_DRIVER_HANDLED. The driver should ensure that the scan line is not in the vertical blank before performing the flip. <b>DdFlip</b> does not affect the actual display of the video data.

If the driver's hardware supports overlays or textures, <b>DdFlip</b> should make any necessary checks based on the surface type before performing the flip.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_flipdata">DD_FLIPDATA</a>