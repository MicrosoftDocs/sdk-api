---
UID: NF:ddraw.IDirectDrawSurface7.IsLost
title: IDirectDrawSurface7::IsLost (ddraw.h)
description: Determines whether the surface memory that is associated with a DirectDrawSurface object has been freed.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","IsLost method","IDirectDrawSurface7.IsLost","IDirectDrawSurface7::IsLost","IsLost","IsLost method [DirectDraw]","IsLost method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::IsLost","directdraw.idirectdrawsurface7_islost"]
old-location: directdraw\idirectdrawsurface7_islost.htm
tech.root: directdraw
ms.assetid: f4654478-ca09-4856-8221-ef5454c23535
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],IsLost method, IDirectDrawSurface7.IsLost, IDirectDrawSurface7::IsLost, IsLost, IsLost method [DirectDraw], IsLost method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::IsLost, directdraw.idirectdrawsurface7_islost
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
 - IDirectDrawSurface7::IsLost
 - ddraw/IDirectDrawSurface7::IsLost
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
 - IDirectDrawSurface7.IsLost
---

# IDirectDrawSurface7::IsLost


## -description

Determines whether the surface memory that is associated with a DirectDrawSurface object has been freed.



## -returns

If the method succeeds, the return value is DD_OK because the memory has not been freed.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACELOST</li>
</ul>
You can use this method to determine when you need to reallocate surface memory. When a DirectDrawSurface object loses its surface memory, most methods return DDERR_SURFACELOST and perform no other action.

## -remarks

Surfaces can lose their memory when the mode of the graphics adapter is changed or when an application receives exclusive access to the graphics adapter and frees all surface memory that is currently allocated on the graphics adapter.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
