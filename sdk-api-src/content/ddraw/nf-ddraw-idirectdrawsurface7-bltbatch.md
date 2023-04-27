---
UID: NF:ddraw.IDirectDrawSurface7.BltBatch
title: IDirectDrawSurface7::BltBatch (ddraw.h)
description: The IDirectDrawSurface7::BltBatch method is not currently implemented.
helpviewer_keywords: ["BltBatch","BltBatch method [DirectDraw]","BltBatch method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","BltBatch method","IDirectDrawSurface7.BltBatch","IDirectDrawSurface7::BltBatch","ddraw/IDirectDrawSurface7::BltBatch","directdraw.idirectdrawsurface7_bltbatch"]
old-location: directdraw\idirectdrawsurface7_bltbatch.htm
tech.root: directdraw
ms.assetid: 50c071a6-2963-474e-994e-c789b1924d92
ms.date: 12/05/2018
ms.keywords: BltBatch, BltBatch method [DirectDraw], BltBatch method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],BltBatch method, IDirectDrawSurface7.BltBatch, IDirectDrawSurface7::BltBatch, ddraw/IDirectDrawSurface7::BltBatch, directdraw.idirectdrawsurface7_bltbatch
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
 - IDirectDrawSurface7::BltBatch
 - ddraw/IDirectDrawSurface7::BltBatch
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
 - IDirectDrawSurface7.BltBatch
---

# IDirectDrawSurface7::BltBatch


## -description

The <b>IDirectDrawSurface7::BltBatch</b> method is not currently implemented.

## -parameters

### -param unnamedParam1 [in]

A pointer to the first <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltbatch">DDBLTBATCH</a> structure that defines the parameters for the bitblt operations.

### -param unnamedParam2 [in]

Number of bitblt operations to be performed.

### -param unnamedParam3 [in]

Currently not used and must be set to 0.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDCLIPLIST</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDRECT</li>
<li>DDERR_NOALPHAHW</li>
<li>DDERR_NOBLTHW</li>
<li>DDERR_NOCLIPLIST</li>
<li>DDERR_NODDROPSHW</li>
<li>DDERR_NOMIRRORHW</li>
<li>DDERR_NORASTEROPHW</li>
<li>DDERR_NOROTATIONHW</li>
<li>DDERR_NOSTRETCHHW</li>
<li>DDERR_NOZBUFFERHW</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>