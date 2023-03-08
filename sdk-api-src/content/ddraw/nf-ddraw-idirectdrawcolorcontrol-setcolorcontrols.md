---
UID: NF:ddraw.IDirectDrawColorControl.SetColorControls
title: IDirectDrawColorControl::SetColorControls (ddraw.h)
description: Sets the color-control options for an overlay or a primary surface.
helpviewer_keywords: ["IDirectDrawColorControl interface [DirectDraw]","SetColorControls method","IDirectDrawColorControl.SetColorControls","IDirectDrawColorControl::SetColorControls","SetColorControls","SetColorControls method [DirectDraw]","SetColorControls method [DirectDraw]","IDirectDrawColorControl interface","ddraw/IDirectDrawColorControl::SetColorControls","directdraw.idirectdrawcolorcontrol_setcolorcontrols"]
old-location: directdraw\idirectdrawcolorcontrol_setcolorcontrols.htm
tech.root: directdraw
ms.assetid: de6f8266-d712-40bd-8230-cf5800cf8926
ms.date: 12/05/2018
ms.keywords: IDirectDrawColorControl interface [DirectDraw],SetColorControls method, IDirectDrawColorControl.SetColorControls, IDirectDrawColorControl::SetColorControls, SetColorControls, SetColorControls method [DirectDraw], SetColorControls method [DirectDraw],IDirectDrawColorControl interface, ddraw/IDirectDrawColorControl::SetColorControls, directdraw.idirectdrawcolorcontrol_setcolorcontrols
f1_keywords:
- ddraw/IDirectDrawColorControl.SetColorControls
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
- IDirectDrawColorControl.SetColorControls
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Sets the color-control options for an overlay or a primary surface.

## -parameters

### -param unnamedParam1 [in]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff549237(v=vs.85)">DDCOLORCONTROL</a> structure that contains the new control settings to apply.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTED</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawcolorcontrol">IDirectDrawColorControl</a>