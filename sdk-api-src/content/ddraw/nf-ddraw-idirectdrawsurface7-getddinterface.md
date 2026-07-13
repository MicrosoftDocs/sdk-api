---
UID: NF:ddraw.IDirectDrawSurface7.GetDDInterface
title: IDirectDrawSurface7::GetDDInterface (ddraw.h)
description: Retrieves an interface to the DirectDraw object that was used to create this surface.
helpviewer_keywords: ["GetDDInterface","GetDDInterface method [DirectDraw]","GetDDInterface method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetDDInterface method","IDirectDrawSurface7.GetDDInterface","IDirectDrawSurface7::GetDDInterface","ddraw/IDirectDrawSurface7::GetDDInterface","directdraw.idirectdrawsurface7_getddinterface"]
old-location: directdraw\idirectdrawsurface7_getddinterface.htm
tech.root: directdraw
ms.assetid: 1ec63614-cdc0-4d07-97e3-97167e7b397c
ms.date: 12/05/2018
ms.keywords: GetDDInterface, GetDDInterface method [DirectDraw], GetDDInterface method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetDDInterface method, IDirectDrawSurface7.GetDDInterface, IDirectDrawSurface7::GetDDInterface, ddraw/IDirectDrawSurface7::GetDDInterface, directdraw.idirectdrawsurface7_getddinterface
f1_keywords:
- ddraw/IDirectDrawSurface7.GetDDInterface
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
- IDirectDrawSurface7.GetDDInterface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawSurface7::GetDDInterface

## -description

Retrieves an interface to the DirectDraw object that was used to create this surface.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives a valid interface pointer if the call succeeds. Cast this pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer; then query for the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a> interface.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks








## -see-also




<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
 

 