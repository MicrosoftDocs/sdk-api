---
UID: NF:ddraw.IDirectDrawSurface7.SetLOD
title: IDirectDrawSurface7::SetLOD (ddraw.h)
description: Sets the maximum level of detail (LOD) for a managed mipmap surface. This method succeeds only on managed textures.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","SetLOD method","IDirectDrawSurface7.SetLOD","IDirectDrawSurface7::SetLOD","SetLOD","SetLOD method [DirectDraw]","SetLOD method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::SetLOD","directdraw.idirectdrawsurface7_setlod"]
old-location: directdraw\idirectdrawsurface7_setlod.htm
tech.root: directdraw
ms.assetid: 596b700f-9a16-4ed0-9ea8-8a1da7d841ae
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],SetLOD method, IDirectDrawSurface7.SetLOD, IDirectDrawSurface7::SetLOD, SetLOD, SetLOD method [DirectDraw], SetLOD method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetLOD, directdraw.idirectdrawsurface7_setlod
f1_keywords:
- ddraw/IDirectDrawSurface7.SetLOD
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
- IDirectDrawSurface7.SetLOD
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Sets the maximum level of detail (LOD) for a managed mipmap surface. This method succeeds only on managed textures.

## -parameters

### -param unnamedParam1 [in]

The maximum LOD value to be set for the mipmap chain if the call succeeds.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks

Applications can call this method only for managed textures (those surfaces that were created with the DDSCAPS2_TEXTUREMANAGE flag). If you call <b>SetLOD</b> on a nonmanaged texture, <b>SetLOD</b> fails and returns DDERR_INVALIDOBJECT.

<b>SetLOD</b> communicates to the Direct3D texture manager the most detailed mipmap in this chain that it should load into local video memory. For example, in a five-level mipmap chain, if you set <i>dwMaxLOD</i> to 2, the texture manager should load only mipmap levels 2 through 4 into local video memory at any given time. Likewise, if the most detailed mipmap in the chain has the dimensions 256×256, setting the maximum level to 2 means that the largest mipmap ever present in video memory has dimensions 64×64.








## -see-also




<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
 

 