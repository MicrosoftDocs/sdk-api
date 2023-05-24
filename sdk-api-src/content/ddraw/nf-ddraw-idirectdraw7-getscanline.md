---
UID: NF:ddraw.IDirectDraw7.GetScanLine
title: IDirectDraw7::GetScanLine (ddraw.h)
description: Retrieves the scan line that is currently being drawn on the monitor.
helpviewer_keywords: ["GetScanLine","GetScanLine method [DirectDraw]","GetScanLine method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","GetScanLine method","IDirectDraw7.GetScanLine","IDirectDraw7::GetScanLine","ddraw/IDirectDraw7::GetScanLine","directdraw.idirectdraw7_getscanline"]
old-location: directdraw\idirectdraw7_getscanline.htm
tech.root: directdraw
ms.assetid: 0bccb384-2de3-49a5-962a-31ad2a751e28
ms.date: 12/05/2018
ms.keywords: GetScanLine, GetScanLine method [DirectDraw], GetScanLine method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetScanLine method, IDirectDraw7.GetScanLine, IDirectDraw7::GetScanLine, ddraw/IDirectDraw7::GetScanLine, directdraw.idirectdraw7_getscanline
f1_keywords:
- ddraw/IDirectDraw7.GetScanLine
dev_langs:
- c++
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ddraw.dll
api_name:
- IDirectDraw7.GetScanLine
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the scan line that is currently being drawn on the monitor.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives the scan line that the display is currently drawing.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_VERTICALBLANKINPROGRESS</li>
</ul>

## -remarks

Scan lines are reported as zero-based integers. The returned scan line value is in the range from 0 through n, where 0 is the first visible scan line on the screen and n is the last visible scan line, plus any scan lines that occur during the vertical blank period. So, in a case where an application is running at a resolution of 640×480 and there are 12 scan lines during vblank, the values returned by this method range from 0 through 491.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>