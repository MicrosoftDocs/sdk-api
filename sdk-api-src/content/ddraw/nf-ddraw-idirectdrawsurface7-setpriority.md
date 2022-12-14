---
UID: NF:ddraw.IDirectDrawSurface7.SetPriority
title: IDirectDrawSurface7::SetPriority (ddraw.h)
description: Assigns the texture-management priority for this texture. This method succeeds only on managed textures.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","SetPriority method","IDirectDrawSurface7.SetPriority","IDirectDrawSurface7::SetPriority","SetPriority","SetPriority method [DirectDraw]","SetPriority method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::SetPriority","directdraw.idirectdrawsurface7_setpriority"]
old-location: directdraw\idirectdrawsurface7_setpriority.htm
tech.root: directdraw
ms.assetid: 06ab2190-db76-41e5-915e-32a3613505a5
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],SetPriority method, IDirectDrawSurface7.SetPriority, IDirectDrawSurface7::SetPriority, SetPriority, SetPriority method [DirectDraw], SetPriority method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetPriority, directdraw.idirectdrawsurface7_setpriority
f1_keywords:
- ddraw/IDirectDrawSurface7.SetPriority
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
- IDirectDrawSurface7.SetPriority
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Assigns the texture-management priority for this texture. This method succeeds only on managed textures.

## -parameters

### -param unnamedParam1 [in]

A value that specifies the new texture-management priority for the texture.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the return value is an error. The method returns DDERR_INVALIDOBJECT if the parameter is invalid or if the texture is not managed by Direct3D.

## -remarks

<b>SetPriority</b> was introduced with the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface.

Priorities are used to determine when managed textures are to be removed from memory. A texture assigned a low priority is removed before a texture with a high priority. If two textures have the same priority, the texture that was used more recently is kept in memory; the other texture is removed.

Applications can set and retrieve priorities only for managed textures (those surfaces that were created with the DDSCAPS2_TEXTUREMANAGE flag). If you call <b>SetPriority</b> on a nonmanaged texture, <b>SetPriority</b> fails and returns DDERR_INVALIDOBJECT.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>