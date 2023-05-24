---
UID: NF:ddraw.IDirectDraw7.Initialize
title: IDirectDraw7::Initialize (ddraw.h)
description: Initializes a DirectDraw object that was created by using the CoCreateInstance COM function.
helpviewer_keywords: ["IDirectDraw7 interface [DirectDraw]","Initialize method","IDirectDraw7.Initialize","IDirectDraw7::Initialize","Initialize","Initialize method [DirectDraw]","Initialize method [DirectDraw]","IDirectDraw7 interface","ddraw/IDirectDraw7::Initialize","directdraw.idirectdraw7_initialize"]
old-location: directdraw\idirectdraw7_initialize.htm
tech.root: directdraw
ms.assetid: e641d8e7-ce29-454a-80fc-d404a27e9b63
ms.date: 12/05/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],Initialize method, IDirectDraw7.Initialize, IDirectDraw7::Initialize, Initialize, Initialize method [DirectDraw], Initialize method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::Initialize, directdraw.idirectdraw7_initialize
f1_keywords:
- ddraw/IDirectDraw7.Initialize
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
- IDirectDraw7.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Initializes a DirectDraw object that was created by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> COM function.

## -parameters

### -param unnamedParam1 [in]

A pointer to the globally unique identifier (GUID) that this method uses as the DirectDraw interface identifier. 

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_ALREADYINITIALIZED</li>
<li>DDERR_DIRECTDRAWALREADYCREATED</li>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NODIRECTDRAWHW</li>
<li>DDERR_NODIRECTDRAWSUPPORT</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>
This method is provided for compliance with the Component Object Model (COM). If you already used the <a href="/windows/desktop/api/ddraw/nf-ddraw-directdrawcreate">DirectDrawCreate</a> function to create a DirectDraw object, this method returns DDERR_ALREADYINITIALIZED. If you do not call <b>IDirectDraw7::Initialize</b> when you use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create a DirectDraw object, any method that you call afterward returns DDERR_NOTINITIALIZED.

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>