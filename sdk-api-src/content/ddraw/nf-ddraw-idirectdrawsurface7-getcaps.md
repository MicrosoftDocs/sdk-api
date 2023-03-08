---
UID: NF:ddraw.IDirectDrawSurface7.GetCaps
title: IDirectDrawSurface7::GetCaps (ddraw.h)
description: Retrieves the capabilities of this surface. These capabilities are not necessarily related to the capabilities of the display device.
helpviewer_keywords: ["GetCaps","GetCaps method [DirectDraw]","GetCaps method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetCaps method","IDirectDrawSurface7.GetCaps","IDirectDrawSurface7::GetCaps","ddraw/IDirectDrawSurface7::GetCaps","directdraw.idirectdrawsurface7_getcaps"]
old-location: directdraw\idirectdrawsurface7_getcaps.htm
tech.root: directdraw
ms.assetid: 971290b7-7df6-41c7-8197-b6169ddd092b
ms.date: 12/05/2018
ms.keywords: GetCaps, GetCaps method [DirectDraw], GetCaps method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetCaps method, IDirectDrawSurface7.GetCaps, IDirectDrawSurface7::GetCaps, ddraw/IDirectDrawSurface7::GetCaps, directdraw.idirectdrawsurface7_getcaps
f1_keywords:
- ddraw/IDirectDrawSurface7.GetCaps
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
- IDirectDrawSurface7.GetCaps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the capabilities of this surface. These capabilities are not necessarily related to the capabilities of the display device.

## -parameters

### -param unnamedParam1 [in]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a> structure that receives the hardware capabilities of this surface.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks

The <b>IDirectDrawSurface7::GetCaps</b> method differs from its counterpart in the <b>IDirectDrawSurface3</b> interface in that it accepts a pointer to a <a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a> structure, rather than the legacy <a href="/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)">DDSCAPS</a> structure.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>