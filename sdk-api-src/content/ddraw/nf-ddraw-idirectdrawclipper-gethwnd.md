---
UID: NF:ddraw.IDirectDrawClipper.GetHWnd
title: IDirectDrawClipper::GetHWnd (ddraw.h)
description: Retrieves the window handle that was previously associated with this DirectDrawClipper object by the IDirectDrawClipper::SetHWnd method.
helpviewer_keywords: ["GetHWnd","GetHWnd method [DirectDraw]","GetHWnd method [DirectDraw]","IDirectDrawClipper interface","IDirectDrawClipper interface [DirectDraw]","GetHWnd method","IDirectDrawClipper.GetHWnd","IDirectDrawClipper::GetHWnd","ddraw/IDirectDrawClipper::GetHWnd","directdraw.idirectdrawclipper_gethwnd"]
old-location: directdraw\idirectdrawclipper_gethwnd.htm
tech.root: directdraw
ms.assetid: 025e898f-e160-4485-87cf-f5fbc014e9f1
ms.date: 12/05/2018
ms.keywords: GetHWnd, GetHWnd method [DirectDraw], GetHWnd method [DirectDraw],IDirectDrawClipper interface, IDirectDrawClipper interface [DirectDraw],GetHWnd method, IDirectDrawClipper.GetHWnd, IDirectDrawClipper::GetHWnd, ddraw/IDirectDrawClipper::GetHWnd, directdraw.idirectdrawclipper_gethwnd
f1_keywords:
- ddraw/IDirectDrawClipper.GetHWnd
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
- IDirectDrawClipper.GetHWnd
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the window handle that was previously associated with this DirectDrawClipper object by the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-sethwnd">IDirectDrawClipper::SetHWnd</a> method.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives the window handle that was previously associated with this DirectDrawClipper object by the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-sethwnd">IDirectDrawClipper::SetHWnd</a> method.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks








## -see-also




<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawclipper">IDirectDrawClipper</a>
 

 