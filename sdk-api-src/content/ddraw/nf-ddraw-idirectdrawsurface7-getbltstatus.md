---
UID: NF:ddraw.IDirectDrawSurface7.GetBltStatus
title: IDirectDrawSurface7::GetBltStatus (ddraw.h)
description: Obtains status about a bit block transfer (bitblt) operation.
helpviewer_keywords: ["DDGBS_CANBLT","DDGBS_ISBLTDONE","GetBltStatus","GetBltStatus method [DirectDraw]","GetBltStatus method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetBltStatus method","IDirectDrawSurface7.GetBltStatus","IDirectDrawSurface7::GetBltStatus","ddraw/IDirectDrawSurface7::GetBltStatus","directdraw.idirectdrawsurface7_getbltstatus"]
old-location: directdraw\idirectdrawsurface7_getbltstatus.htm
tech.root: directdraw
ms.assetid: 1f446300-065b-47c1-9778-fb4a5b2ea4bd
ms.date: 12/05/2018
ms.keywords: DDGBS_CANBLT, DDGBS_ISBLTDONE, GetBltStatus, GetBltStatus method [DirectDraw], GetBltStatus method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetBltStatus method, IDirectDrawSurface7.GetBltStatus, IDirectDrawSurface7::GetBltStatus, ddraw/IDirectDrawSurface7::GetBltStatus, directdraw.idirectdrawsurface7_getbltstatus
f1_keywords:
- ddraw/IDirectDrawSurface7.GetBltStatus
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
- IDirectDrawSurface7.GetBltStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Obtains status about a bit block transfer (bitblt) operation.

## -parameters

### -param unnamedParam1 [in]

A value that can be set to one of the following flags.

#### DDGBS_CANBLT

Inquires whether a bitblt that involves this surface can occur immediately, and returns DD_OK if the bitblt can be completed.

#### DDGBS_ISBLTDONE

Inquires whether the bitblt is done, and returns DD_OK if the last bitblt on this surface has completed.

## -returns

If the method succeeds, a bitbltter is present, and the return value is DD_OK.

If it fails, the method returns DDERR_WASSTILLDRAWING if the bitbltter is busy, DDERR_NOBLTHW if there is no bitbltter, or one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOBLTHW</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>