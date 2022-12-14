---
UID: NF:ddraw.IDirectDrawGammaControl.SetGammaRamp
title: IDirectDrawGammaControl::SetGammaRamp (ddraw.h)
description: Sets the red, green, and blue gamma ramps for the primary surface.
helpviewer_keywords: ["IDirectDrawGammaControl interface [DirectDraw]","SetGammaRamp method","IDirectDrawGammaControl.SetGammaRamp","IDirectDrawGammaControl::SetGammaRamp","SetGammaRamp","SetGammaRamp method [DirectDraw]","SetGammaRamp method [DirectDraw]","IDirectDrawGammaControl interface","ddraw/IDirectDrawGammaControl::SetGammaRamp","directdraw.idirectdrawgammacontrol_setgammaramp"]
old-location: directdraw\idirectdrawgammacontrol_setgammaramp.htm
tech.root: directdraw
ms.assetid: 3bde7ba7-8498-42e5-bd5a-625e162fc1db
ms.date: 12/05/2018
ms.keywords: IDirectDrawGammaControl interface [DirectDraw],SetGammaRamp method, IDirectDrawGammaControl.SetGammaRamp, IDirectDrawGammaControl::SetGammaRamp, SetGammaRamp, SetGammaRamp method [DirectDraw], SetGammaRamp method [DirectDraw],IDirectDrawGammaControl interface, ddraw/IDirectDrawGammaControl::SetGammaRamp, directdraw.idirectdrawgammacontrol_setgammaramp
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
 - IDirectDrawGammaControl::SetGammaRamp
 - ddraw/IDirectDrawGammaControl::SetGammaRamp
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
 - IDirectDrawGammaControl.SetGammaRamp
---

# IDirectDrawGammaControl::SetGammaRamp


## -description

Sets the red, green, and blue gamma ramps for the primary surface.

## -parameters

### -param unnamedParam1 [in]

Flag that indicates whether gamma calibration is required. Set this parameter to DDSGR_CALIBRATE to request that the calibrator adjust the gamma ramp according to the physical properties of the display, which makes the result identical on all computers. If calibration is not needed, set this parameter to 0.

### -param unnamedParam2 [in]

A pointer to a <a href="/windows/desktop/api/ddraw/ns-ddraw-ddgammaramp">DDGAMMARAMP</a> structure that contains the new red, green, and blue gamma ramp entries. Each array maps color values in the frame buffer to the color values to be passed to the digital-to-analog converter (DAC).

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXCEPTION</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>

## -remarks

Not all systems support gamma calibration. To determine whether gamma calibration is supported, call <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getcaps">IDirectDraw7::GetCaps</a> and examine the <b>dwCaps2</b> member of the associated <a href="/windows/desktop/api/ddraw/ns-ddraw-ddcaps_dx3">DDCAPS</a> structure after the method returns. If the DDCAPS2_CANCALIBRATEGAMMA capability flag is present, gamma calibration is supported.



Calibrating gamma ramps incurs some processing overhead and should not be used frequently.

Including the DDSGR_CALIBRATE flag in the <i>dwFlags</i> parameter when running on computers that do not support gamma calibration does not cause this method to fail. The method succeeds and sets new gamma ramp values without calibration.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawgammacontrol">IDirectDrawGammaControl</a>