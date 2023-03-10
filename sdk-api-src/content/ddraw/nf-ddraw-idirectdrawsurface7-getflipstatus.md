---
UID: NF:ddraw.IDirectDrawSurface7.GetFlipStatus
title: IDirectDrawSurface7::GetFlipStatus (ddraw.h)
description: Retrieves status about whether this surface has finished its flipping process.
helpviewer_keywords: ["DDGFS_CANFLIP","DDGFS_ISFLIPDONE","GetFlipStatus","GetFlipStatus method [DirectDraw]","GetFlipStatus method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetFlipStatus method","IDirectDrawSurface7.GetFlipStatus","IDirectDrawSurface7::GetFlipStatus","ddraw/IDirectDrawSurface7::GetFlipStatus","directdraw.idirectdrawsurface7_getflipstatus"]
old-location: directdraw\idirectdrawsurface7_getflipstatus.htm
tech.root: directdraw
ms.assetid: e337bdde-bf63-414a-88a5-507478476667
ms.date: 12/05/2018
ms.keywords: DDGFS_CANFLIP, DDGFS_ISFLIPDONE, GetFlipStatus, GetFlipStatus method [DirectDraw], GetFlipStatus method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetFlipStatus method, IDirectDrawSurface7.GetFlipStatus, IDirectDrawSurface7::GetFlipStatus, ddraw/IDirectDrawSurface7::GetFlipStatus, directdraw.idirectdrawsurface7_getflipstatus
f1_keywords:
- ddraw/IDirectDrawSurface7.GetFlipStatus
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
- IDirectDrawSurface7.GetFlipStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves status about whether this surface has finished its flipping process.

## -parameters

### -param unnamedParam1 [in]

A value that can be set to one of the following flags:

#### DDGFS_CANFLIP

Inquires whether this surface can be flipped immediately, and returns DD_OK if the flip can be completed.

#### DDGFS_ISFLIPDONE

Inquires whether the flip has finished, and returns DD_OK if the last flip on this surface has completed.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return DDERR_WASSTILLDRAWING if the surface has not finished its flipping process, or one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>