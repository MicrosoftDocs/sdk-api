---
UID: NF:ddraw.IDirectDrawSurface7.UpdateOverlayZOrder
title: IDirectDrawSurface7::UpdateOverlayZOrder (ddraw.h)
description: Sets the z-order of an overlay.
helpviewer_keywords: ["DDOVERZ_INSERTINBACKOF","DDOVERZ_INSERTINFRONTOF","DDOVERZ_MOVEBACKWARD","DDOVERZ_MOVEFORWARD","DDOVERZ_SENDTOBACK","DDOVERZ_SENDTOFRONT","IDirectDrawSurface7 interface [DirectDraw]","UpdateOverlayZOrder method","IDirectDrawSurface7.UpdateOverlayZOrder","IDirectDrawSurface7::UpdateOverlayZOrder","UpdateOverlayZOrder","UpdateOverlayZOrder method [DirectDraw]","UpdateOverlayZOrder method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::UpdateOverlayZOrder","directdraw.idirectdrawsurface7_updateoverlayzorder"]
old-location: directdraw\idirectdrawsurface7_updateoverlayzorder.htm
tech.root: directdraw
ms.assetid: a95f315f-7a1f-4ca0-bb18-9bd54f2cc78d
ms.date: 12/05/2018
ms.keywords: DDOVERZ_INSERTINBACKOF, DDOVERZ_INSERTINFRONTOF, DDOVERZ_MOVEBACKWARD, DDOVERZ_MOVEFORWARD, DDOVERZ_SENDTOBACK, DDOVERZ_SENDTOFRONT, IDirectDrawSurface7 interface [DirectDraw],UpdateOverlayZOrder method, IDirectDrawSurface7.UpdateOverlayZOrder, IDirectDrawSurface7::UpdateOverlayZOrder, UpdateOverlayZOrder, UpdateOverlayZOrder method [DirectDraw], UpdateOverlayZOrder method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::UpdateOverlayZOrder, directdraw.idirectdrawsurface7_updateoverlayzorder
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
 - IDirectDrawSurface7::UpdateOverlayZOrder
 - ddraw/IDirectDrawSurface7::UpdateOverlayZOrder
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
 - IDirectDrawSurface7.UpdateOverlayZOrder
---

# IDirectDrawSurface7::UpdateOverlayZOrder


## -description

Sets the z-order of an overlay.

## -parameters

### -param unnamedParam1 [in]

One of the following flags that determines the z-order of the overlay:



#### DDOVERZ_INSERTINBACKOF

Inserts this overlay in the overlay chain behind the reference overlay.



#### DDOVERZ_INSERTINFRONTOF

Inserts this overlay in the overlay chain in front of the reference overlay.



#### DDOVERZ_MOVEBACKWARD

Moves this overlay one position backward in the overlay chain.



#### DDOVERZ_MOVEFORWARD

Moves this overlay one position forward in the overlay chain.



#### DDOVERZ_SENDTOBACK

Moves this overlay to the back of the overlay chain.



#### DDOVERZ_SENDTOFRONT

Moves this overlay to the front of the overlay chain.

### -param unnamedParam2 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for the DirectDraw surface to be used as a relative position in the overlay chain. This parameter is needed only for the DDOVERZ_INSERTINBACKOF and DDOVERZ_INSERTINFRONTOF flags.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTAOVERLAYSURFACE</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>