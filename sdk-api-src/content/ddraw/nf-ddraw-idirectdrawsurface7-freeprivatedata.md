---
UID: NF:ddraw.IDirectDrawSurface7.FreePrivateData
title: IDirectDrawSurface7::FreePrivateData (ddraw.h)
description: Frees the specified private data that is associated with this surface.
helpviewer_keywords: ["FreePrivateData","FreePrivateData method [DirectDraw]","FreePrivateData method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","FreePrivateData method","IDirectDrawSurface7.FreePrivateData","IDirectDrawSurface7::FreePrivateData","ddraw/IDirectDrawSurface7::FreePrivateData","directdraw.idirectdrawsurface7_freeprivatedata"]
old-location: directdraw\idirectdrawsurface7_freeprivatedata.htm
tech.root: directdraw
ms.assetid: 66d3f701-735c-4dca-b7b6-47a17d63c23e
ms.date: 12/05/2018
ms.keywords: FreePrivateData, FreePrivateData method [DirectDraw], FreePrivateData method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],FreePrivateData method, IDirectDrawSurface7.FreePrivateData, IDirectDrawSurface7::FreePrivateData, ddraw/IDirectDrawSurface7::FreePrivateData, directdraw.idirectdrawsurface7_freeprivatedata
f1_keywords:
- ddraw/IDirectDrawSurface7.FreePrivateData
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
- IDirectDrawSurface7.FreePrivateData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Frees the specified private data that is associated with this surface.

## -parameters

### -param unnamedParam1 [in]

Reference to (C++) or address of (C) the globally unique identifier that identifies the private data to be freed.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTFOUND</li>
</ul>

## -remarks

DirectDraw calls this method automatically when a surface is released.

If the private data was set by using the DDSPD_IUNKNOWNPOINTER flag, <b>FreePrivateData</b> calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the associated interface.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>