---
UID: NF:winddi.DrvDisableDirectDraw
title: DrvDisableDirectDraw function (winddi.h)
description: The DrvDisableDirectDraw function disables hardware for DirectDraw use.
helpviewer_keywords: ["DrvDisableDirectDraw","DrvDisableDirectDraw function [Display Devices]","ddfncs_7abbe471-0671-4e98-8eba-ceb25216d961.xml","display.drvdisabledirectdraw","winddi/DrvDisableDirectDraw"]
old-location: display\drvdisabledirectdraw.htm
tech.root: display
ms.assetid: 7675019e-ac05-40e8-a934-a0928800ebe3
ms.date: 12/05/2018
ms.keywords: DrvDisableDirectDraw, DrvDisableDirectDraw function [Display Devices], ddfncs_7abbe471-0671-4e98-8eba-ceb25216d961.xml, display.drvdisabledirectdraw, winddi/DrvDisableDirectDraw
req.header: winddi.h
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
 - DrvDisableDirectDraw
 - winddi/DrvDisableDirectDraw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvDisableDirectDraw
---

# DrvDisableDirectDraw function


## -description

The <b>DrvDisableDirectDraw</b> function disables hardware for DirectDraw use.

## -parameters

### -param dhpdev

Handle to the <a href="/windows-hardware/drivers/">PDEV</a> that was returned by the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a> routine.

## -remarks

GDI calls the driver's <b>DrvDisableDirectDraw</b> function when the last DirectDraw application has finished running. A driver's <b>DrvDisableDirectDraw</b> implementation should clean up any software resources and reclaim any hardware resources that the driver dedicated to DirectDraw in its <a href="/windows/desktop/api/winddi/nf-winddi-drvenabledirectdraw">DrvEnableDirectDraw</a> function.

<b>DrvDisableDirectDraw</b> can be called with a disabled <a href="/windows-hardware/drivers/">PDEV</a>. A PDEV is disabled or enabled by calling the display driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvassertmode">DrvAssertMode</a> function. See <a href="/windows-hardware/drivers/display/managing-pdevs">Managing PDEVs</a> for more information.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenabledirectdraw">DrvEnableDirectDraw</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>