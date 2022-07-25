---
UID: NC:ddrawint.PDD_MOCOMPCB_RENDER
title: PDD_MOCOMPCB_RENDER (ddrawint.h)
description: The DdMoCompRender callback function tells the driver what macroblocks to render by specifying the surfaces containing the macroblocks, the offsets in each surface where the macroblocks exist, and the size of the macroblock data to be rendered.
helpviewer_keywords: ["DdMoCompRender","DdMoCompRender callback function [Display Devices]","PDD_MOCOMPCB_RENDER","PDD_MOCOMPCB_RENDER callback","ddfncs_60970586-34af-4e35-a963-98220fc7ef43.xml","ddrawint/DdMoCompRender","display.ddmocomprender"]
old-location: display\ddmocomprender.htm
tech.root: display
ms.assetid: d88f2c7e-e3e5-4444-836c-a45d52c86e54
ms.date: 12/05/2018
ms.keywords: DdMoCompRender, DdMoCompRender callback function [Display Devices], PDD_MOCOMPCB_RENDER, PDD_MOCOMPCB_RENDER callback, ddfncs_60970586-34af-4e35-a963-98220fc7ef43.xml, ddrawint/DdMoCompRender, display.ddmocomprender
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
 - PDD_MOCOMPCB_RENDER
 - ddrawint/PDD_MOCOMPCB_RENDER
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
 - DdMoCompRender
---

## -description

The <b>DdMoCompRender</b> callback function tells the driver what macroblocks to render by specifying the surfaces containing the macroblocks, the offsets in each surface where the macroblocks exist, and the size of the macroblock data to be rendered.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_rendermocompdata">DD_RENDERMOCOMPDATA</a> structure that contains the information needed to render a frame.

## -returns

<b>DdMoCompRender</b> returns one of the following callback codes:

## -remarks

DirectDraw drivers that support motion compensation must implement <b>DdMoCompRender</b>.

<b>DdMoCompRender</b> can be called multiple times between the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_beginframe">DdMoCompBeginFrame</a> and <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_endframe">DdMoCompEndFrame</a> sequence.

If a previous render operation is not yet finished, the driver should fail the call by setting the <b>ddRVal</b> member of the DD_RENDERMOCOMPDATA structure at <i>lpRenderData</i> to DDERR_WASSTILLDRAWING and returning DDHAL_DRIVER_HANDLED.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_rendermocompdata">DD_RENDERMOCOMPDATA</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_beginframe">DdMoCompBeginFrame</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_endframe">DdMoCompEndFrame</a>