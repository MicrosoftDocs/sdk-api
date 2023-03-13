---
UID: NF:ddraw.IDirectDrawGammaControl.GetGammaRamp
title: IDirectDrawGammaControl::GetGammaRamp (ddraw.h)
description: Retrieves the red, green, and blue gamma ramps for the primary surface.
helpviewer_keywords: ["GetGammaRamp","GetGammaRamp method [DirectDraw]","GetGammaRamp method [DirectDraw]","IDirectDrawGammaControl interface","IDirectDrawGammaControl interface [DirectDraw]","GetGammaRamp method","IDirectDrawGammaControl.GetGammaRamp","IDirectDrawGammaControl::GetGammaRamp","ddraw/IDirectDrawGammaControl::GetGammaRamp","directdraw.idirectdrawgammacontrol_getgammaramp"]
old-location: directdraw\idirectdrawgammacontrol_getgammaramp.htm
tech.root: directdraw
ms.assetid: ba83605c-c388-42c0-9297-1666c80a278e
ms.date: 12/05/2018
ms.keywords: GetGammaRamp, GetGammaRamp method [DirectDraw], GetGammaRamp method [DirectDraw],IDirectDrawGammaControl interface, IDirectDrawGammaControl interface [DirectDraw],GetGammaRamp method, IDirectDrawGammaControl.GetGammaRamp, IDirectDrawGammaControl::GetGammaRamp, ddraw/IDirectDrawGammaControl::GetGammaRamp, directdraw.idirectdrawgammacontrol_getgammaramp
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
 - IDirectDrawGammaControl::GetGammaRamp
 - ddraw/IDirectDrawGammaControl::GetGammaRamp
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
 - IDirectDrawGammaControl.GetGammaRamp
---

# IDirectDrawGammaControl::GetGammaRamp


## -description

Retrieves the red, green, and blue gamma ramps for the primary surface.

## -parameters

### -param unnamedParam1 [in]

Currently not used and must be set to 0.

### -param unnamedParam2 [in, out]

A pointer to a <a href="/windows/desktop/api/ddraw/ns-ddraw-ddgammaramp">DDGAMMARAMP</a> structure that receives the current red, green, and blue gamma ramps. Each array maps color values in the frame buffer to the color values to be passed to the digital-to-analog converter (DAC).

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXCEPTION</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawgammacontrol">IDirectDrawGammaControl</a>