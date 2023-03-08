---
UID: NF:ddraw.IDirectDrawPalette.Initialize
title: IDirectDrawPalette::Initialize (ddraw.h)
description: Initializes the DirectDrawPalette object.
helpviewer_keywords: ["IDirectDrawPalette interface [DirectDraw]","Initialize method","IDirectDrawPalette.Initialize","IDirectDrawPalette::Initialize","Initialize","Initialize method [DirectDraw]","Initialize method [DirectDraw]","IDirectDrawPalette interface","ddraw/IDirectDrawPalette::Initialize","directdraw.idirectdrawpalette_initialize"]
old-location: directdraw\idirectdrawpalette_initialize.htm
tech.root: directdraw
ms.assetid: e0ad7ea1-759d-48e9-8d15-6601d9b15588
ms.date: 12/05/2018
ms.keywords: IDirectDrawPalette interface [DirectDraw],Initialize method, IDirectDrawPalette.Initialize, IDirectDrawPalette::Initialize, Initialize, Initialize method [DirectDraw], Initialize method [DirectDraw],IDirectDrawPalette interface, ddraw/IDirectDrawPalette::Initialize, directdraw.idirectdrawpalette_initialize
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
 - IDirectDrawPalette::Initialize
 - ddraw/IDirectDrawPalette::Initialize
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
 - IDirectDrawPalette.Initialize
---

# IDirectDrawPalette::Initialize


## -description

Initializes the DirectDrawPalette object.

## -parameters

### -param unnamedParam1 [in]

A pointer to the DirectDraw object to associate with the DirectDrawPalette object.

### -param unnamedParam2 [in]

Currently not used and must be set to 0.

### -param unnamedParam3 [out]

Currently not used and must be set to NULL.

## -returns

This method returns DDERR_ALREADYINITIALIZED.

This method is provided for compliance with the Component Object Model (COM). Because the DirectDrawPalette object is initialized when it is created, this method always returns DDERR_ALREADYINITIALIZED.

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawpalette">IDirectDrawPalette</a>