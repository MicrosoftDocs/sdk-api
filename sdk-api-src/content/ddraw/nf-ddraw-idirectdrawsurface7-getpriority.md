---
UID: NF:ddraw.IDirectDrawSurface7.GetPriority
title: IDirectDrawSurface7::GetPriority (ddraw.h)
description: Retrieves the texture-management priority for this texture. This method succeeds only on managed textures.
helpviewer_keywords: ["GetPriority","GetPriority method [DirectDraw]","GetPriority method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetPriority method","IDirectDrawSurface7.GetPriority","IDirectDrawSurface7::GetPriority","ddraw/IDirectDrawSurface7::GetPriority","directdraw.idirectdrawsurface7_getpriority"]
old-location: directdraw\idirectdrawsurface7_getpriority.htm
tech.root: directdraw
ms.assetid: 59a47305-92d5-42a3-9ad1-11c80e3744df
ms.date: 12/05/2018
ms.keywords: GetPriority, GetPriority method [DirectDraw], GetPriority method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetPriority method, IDirectDrawSurface7.GetPriority, IDirectDrawSurface7::GetPriority, ddraw/IDirectDrawSurface7::GetPriority, directdraw.idirectdrawsurface7_getpriority
f1_keywords:
- ddraw/IDirectDrawSurface7.GetPriority
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
- IDirectDrawSurface7.GetPriority
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the texture-management priority for this texture. This method succeeds only on managed textures.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives the texture priority if the call succeeds.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the return value is an error. The method returns DDERR_INVALIDOBJECT if the parameter is invalid or if the texture is not managed by Direct3D.

## -remarks

Priorities are used to determine when managed textures are to be removed from memory. A texture assigned a low priority is removed before a texture with a high priority. If two textures have the same priority, the texture that was used more recently is kept in memory; the other texture is removed.

Applications can set and retrieve priorities only for managed textures (those surfaces that were created with the DDSCAPS2_TEXTUREMANAGE flag). If you call <b>GetPriority</b> on a nonmanaged texture, <b>GetPriority</b> fails and returns DDERR_INVALIDOBJECT.

<b>GetPriority</b> was introduced with the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>