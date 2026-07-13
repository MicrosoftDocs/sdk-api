---
UID: NF:ddraw.IDirectDrawSurface7.Initialize
title: IDirectDrawSurface7::Initialize (ddraw.h)
description: Initializes a DirectDrawSurface object.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","Initialize method","IDirectDrawSurface7.Initialize","IDirectDrawSurface7::Initialize","Initialize","Initialize method [DirectDraw]","Initialize method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::Initialize","directdraw.idirectdrawsurface7_initialize"]
old-location: directdraw\idirectdrawsurface7_initialize.htm
tech.root: directdraw
ms.assetid: 98b9a05f-ff61-4c58-9c09-625077eb64ad
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],Initialize method, IDirectDrawSurface7.Initialize, IDirectDrawSurface7::Initialize, Initialize, Initialize method [DirectDraw], Initialize method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::Initialize, directdraw.idirectdrawsurface7_initialize
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
 - IDirectDrawSurface7::Initialize
 - ddraw/IDirectDrawSurface7::Initialize
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
 - IDirectDrawSurface7.Initialize
---

# IDirectDrawSurface7::Initialize


## -description

Initializes a DirectDrawSurface object.

## -parameters

### -param unnamedParam1 [in]

A pointer to the DirectDraw object to associate with the DirectDrawSurface object.

### -param unnamedParam2 [in]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that describes how to initialize this surface.

## -returns

This method returns DDERR_ALREADYINITIALIZED.

This method is provided for compliance with the Component Object Model (COM). Because the DirectDrawSurface object is initialized when it is created, this method always returns DDERR_ALREADYINITIALIZED.

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>