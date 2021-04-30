---
UID: NC:ddrawint.PDD_COLORCB_COLORCONTROL
title: PDD_COLORCB_COLORCONTROL (ddrawint.h)
description: The DdControlColor callback function controls the luminance and brightness controls of an overlay surface.
helpviewer_keywords: ["DdControlColor","DdControlColor callback function [Display Devices]","PDD_COLORCB_COLORCONTROL","PDD_COLORCB_COLORCONTROL callback","ddfncs_c79505e9-282b-469f-ae35-19a9644aecae.xml","ddrawint/DdControlColor","display.ddcontrolcolor"]
old-location: display\ddcontrolcolor.htm
tech.root: display
ms.assetid: 626fdd37-bebb-47b7-9899-7cf0dc2bd1ba
ms.date: 12/05/2018
ms.keywords: DdControlColor, DdControlColor callback function [Display Devices], PDD_COLORCB_COLORCONTROL, PDD_COLORCB_COLORCONTROL callback, ddfncs_c79505e9-282b-469f-ae35-19a9644aecae.xml, ddrawint/DdControlColor, display.ddcontrolcolor
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
 - PDD_COLORCB_COLORCONTROL
 - ddrawint/PDD_COLORCB_COLORCONTROL
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
 - DdControlColor
---

## -description

The <b>DdControlColor</b> callback function controls the luminance and brightness controls of an overlay surface.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontroldata">DD_COLORCONTROLDATA</a> structure that contains the color control information for a specified overlay surface.

## -returns

<b>DdControlColor</b> returns a callback code.

## -remarks

<b>DdControlColor</b> can be optionally implemented in a DirectDraw driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontroldata">DD_COLORCONTROLDATA</a>