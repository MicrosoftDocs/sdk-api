---
UID: NF:winddi.DrvSwapBuffers
title: DrvSwapBuffers function (winddi.h)
description: The DrvSwapBuffers function displays the contents of the window's associated hidden buffer on the specified surface.
helpviewer_keywords: ["DrvSwapBuffers","DrvSwapBuffers function [Display Devices]","ddifncs_8f9d0c15-6eb3-4bed-9efa-bb40026576a1.xml","display.drvswapbuffers","winddi/DrvSwapBuffers"]
old-location: display\drvswapbuffers.htm
tech.root: display
ms.assetid: 2fee2f9d-85fd-4b21-83be-11469fede71a
ms.date: 12/05/2018
ms.keywords: DrvSwapBuffers, DrvSwapBuffers function [Display Devices], ddifncs_8f9d0c15-6eb3-4bed-9efa-bb40026576a1.xml, display.drvswapbuffers, winddi/DrvSwapBuffers
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
 - DrvSwapBuffers
 - winddi/DrvSwapBuffers
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
 - DrvSwapBuffers
---

# DrvSwapBuffers function


## -description

The <b>DrvSwapBuffers</b> function displays the contents of the window's associated hidden buffer on the specified surface.

## -parameters

### -param pso

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that identifies the target surface to be modified for display.

### -param pwo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a> structure that defines the region on the target surface with which the back buffer will be swapped.

## -returns

The return value is <b>TRUE</b> if the function is successful; it is <b>FALSE</b> upon failure.

## -remarks

<b>DrvSwapBuffers</b> can affect the display only if the pixel format for the window specified by <i>pwo</i> is double-buffered. The content of the hidden buffer is undefined after the swap occurs.

This function is required if the driver supports a pixel format with double buffering; that is, if PFD_DOUBLEBUFFER is set in the <b>dwFlags</b> member of the PIXELFORMATDESCRIPTOR structure.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvdescribepixelformat">DrvDescribePixelFormat</a>