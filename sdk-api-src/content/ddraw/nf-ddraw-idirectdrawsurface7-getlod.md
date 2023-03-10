---
UID: NF:ddraw.IDirectDrawSurface7.GetLOD
title: IDirectDrawSurface7::GetLOD (ddraw.h)
description: Retrieves the maximum level of detail (LOD) currently set for a managed mipmap surface. This method succeeds only on managed textures.
helpviewer_keywords: ["GetLOD","GetLOD method [DirectDraw]","GetLOD method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetLOD method","IDirectDrawSurface7.GetLOD","IDirectDrawSurface7::GetLOD","ddraw/IDirectDrawSurface7::GetLOD","directdraw.idirectdrawsurface7_getlod"]
old-location: directdraw\idirectdrawsurface7_getlod.htm
tech.root: directdraw
ms.assetid: 9208372b-47ac-4079-9e4a-28cf51912a93
ms.date: 12/05/2018
ms.keywords: GetLOD, GetLOD method [DirectDraw], GetLOD method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetLOD method, IDirectDrawSurface7.GetLOD, IDirectDrawSurface7::GetLOD, ddraw/IDirectDrawSurface7::GetLOD, directdraw.idirectdrawsurface7_getlod
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
 - IDirectDrawSurface7::GetLOD
 - ddraw/IDirectDrawSurface7::GetLOD
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
 - IDirectDrawSurface7.GetLOD
---

## -description

Retrieves the maximum level of detail (LOD) currently set for a managed mipmap surface. This method succeeds only on managed textures.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives the maximum LOD value if the call succeeds.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks

Applications can call this method only for managed textures (those surfaces that were created with the DDSCAPS2_TEXTUREMANAGE flag). If you call <b>GetLOD</b> on a nonmanaged texture, <b>GetLOD</b> fails and returns DDERR_INVALIDOBJECT.

<b>GetLOD</b> communicates to the Direct3D texture manager the most detailed mipmap in this chain that it should load into local video memory. For example, in a five-level mipmap chain, a value of 2 in the variable at <i>lpdwMaxLOD</i> indicates that the texture manager loads only mipmap levels 2 through 4 into local video memory at any given time. Likewise, if the most detailed mipmap in the chain has the dimensions 256×256, a value of 2 in <i>lpdwMaxLOD</i> means that the largest mipmap ever present in video memory has dimensions 64×64.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>