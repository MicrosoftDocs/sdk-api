---
UID: NF:ddraw.IDirectDraw7.RestoreAllSurfaces
title: IDirectDraw7::RestoreAllSurfaces (ddraw.h)
description: Restores all the surfaces that were created for the DirectDraw object, in the order that they were created.
helpviewer_keywords: ["IDirectDraw7 interface [DirectDraw]","RestoreAllSurfaces method","IDirectDraw7.RestoreAllSurfaces","IDirectDraw7::RestoreAllSurfaces","RestoreAllSurfaces","RestoreAllSurfaces method [DirectDraw]","RestoreAllSurfaces method [DirectDraw]","IDirectDraw7 interface","ddraw/IDirectDraw7::RestoreAllSurfaces","directdraw.idirectdraw7_restoreallsurfaces"]
old-location: directdraw\idirectdraw7_restoreallsurfaces.htm
tech.root: directdraw
ms.assetid: 72897004-cd44-4ca4-bc28-a49bffc09c76
ms.date: 12/05/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],RestoreAllSurfaces method, IDirectDraw7.RestoreAllSurfaces, IDirectDraw7::RestoreAllSurfaces, RestoreAllSurfaces, RestoreAllSurfaces method [DirectDraw], RestoreAllSurfaces method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::RestoreAllSurfaces, directdraw.idirectdraw7_restoreallsurfaces
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
 - IDirectDraw7::RestoreAllSurfaces
 - ddraw/IDirectDraw7::RestoreAllSurfaces
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
 - IDirectDraw7.RestoreAllSurfaces
---

# IDirectDraw7::RestoreAllSurfaces


## -description

 Restores all the surfaces that were created for the DirectDraw object, in the order that they were created.



## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks

This method is provided for convenience. Effectively, this method calls the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-restore">IDirectDrawSurface7::Restore</a> method for each surface that is created by this DirectDraw object.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>
