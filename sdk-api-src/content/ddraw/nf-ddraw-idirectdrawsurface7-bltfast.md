---
UID: NF:ddraw.IDirectDrawSurface7.BltFast
title: IDirectDrawSurface7::BltFast (ddraw.h)
description: Performs a source copy bitblt or transparent bitblt by using a source color key or destination color key.
helpviewer_keywords: ["BltFast","BltFast method [DirectDraw]","BltFast method [DirectDraw]","IDirectDrawSurface7 interface","DDBLTFAST_DESTCOLORKEY","DDBLTFAST_NOCOLORKEY","DDBLTFAST_SRCCOLORKEY","DDBLTFAST_WAIT","IDirectDrawSurface7 interface [DirectDraw]","BltFast method","IDirectDrawSurface7.BltFast","IDirectDrawSurface7::BltFast","ddraw/IDirectDrawSurface7::BltFast","directdraw.idirectdrawsurface7_bltfast"]
old-location: directdraw\idirectdrawsurface7_bltfast.htm
tech.root: directdraw
ms.assetid: ac882b48-87b2-4b65-99b0-ac9065b5f47f
ms.date: 12/05/2018
ms.keywords: BltFast, BltFast method [DirectDraw], BltFast method [DirectDraw],IDirectDrawSurface7 interface, DDBLTFAST_DESTCOLORKEY, DDBLTFAST_NOCOLORKEY, DDBLTFAST_SRCCOLORKEY, DDBLTFAST_WAIT, IDirectDrawSurface7 interface [DirectDraw],BltFast method, IDirectDrawSurface7.BltFast, IDirectDrawSurface7::BltFast, ddraw/IDirectDrawSurface7::BltFast, directdraw.idirectdrawsurface7_bltfast
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawSurface7::BltFast
 - ddraw/IDirectDrawSurface7::BltFast
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawSurface7.BltFast
---

# IDirectDrawSurface7::BltFast


## -description

Performs a source copy bitblt or transparent bitblt by using a source color key or destination color key.

## -parameters

### -param unnamedParam1 [in]

The x-coordinate to bitblt to on the destination surface.

### -param unnamedParam2 [in]

The y-coordinate to bitblt to on the destination surface.

### -param unnamedParam3 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for the DirectDrawSurface object that is the source of the bitblt.

### -param unnamedParam4 [in]

A pointer to a <b>RECT</b> structure that defines the upper-left and lower-right points of the rectangle to bitblt from on the source surface.

### -param unnamedParam5 [in]

Type of transfer. The following transfers are defined:



#### DDBLTFAST_DESTCOLORKEY

A transparent bitblt that uses the destination color key.



#### DDBLTFAST_NOCOLORKEY

A normal copy bitblt with no transparency.



#### DDBLTFAST_SRCCOLORKEY

A transparent bitblt that uses the source color key.



#### DDBLTFAST_WAIT

Postpones the DDERR_WASSTILLDRAWING message if the bitbltter is busy, and returns as soon as the bitblt can be set up or another error occurs.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXCEPTION</li>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDRECT</li>
<li>DDERR_NOBLTHW</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>

## -remarks

<b>BltFast</b> always attempts an asynchronous blit if it is supported by the hardware.

<b>BltFast</b> works only on display memory surfaces and cannot clip when it performs a bitblt operation. If you use this method on a surface with an attached clipper, the call fails, and the method returns DDERR_UNSUPPORTED.

The software implementation of <b>IDirectDrawSurface7::BltFast</b> is 10 percent faster than the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-blt">IDirectDrawSurface7::Blt</a> method. However, there is no speed difference between the two if display hardware is used.

Typically, <b>IDirectDrawSurface7::BltFast</b> returns immediately with an error if the bitbltter is busy and the bitblt cannot be set up. You can use the DDBLTFAST_WAIT flag, however, if you want this method not to return until either the bitblt can be set up or another error occurs.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>