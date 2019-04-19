---
UID: NF:ddraw.IDirectDrawGammaControl.SetGammaRamp
title: IDirectDrawGammaControl::SetGammaRamp (ddraw.h)
author: windows-sdk-content
description: Sets the red, green, and blue gamma ramps for the primary surface.
old-location: directdraw\idirectdrawgammacontrol_setgammaramp.htm
tech.root: directdraw
ms.assetid: 3bde7ba7-8498-42e5-bd5a-625e162fc1db
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectDrawGammaControl interface [DirectDraw],SetGammaRamp method, IDirectDrawGammaControl.SetGammaRamp, IDirectDrawGammaControl::SetGammaRamp, SetGammaRamp, SetGammaRamp method [DirectDraw], SetGammaRamp method [DirectDraw],IDirectDrawGammaControl interface, ddraw/IDirectDrawGammaControl::SetGammaRamp, directdraw.idirectdrawgammacontrol_setgammaramp
ms.topic: method
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
 - IDirectDrawGammaControl.SetGammaRamp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawGammaControl::SetGammaRamp


## -description


Sets the red, green, and blue gamma ramps for the primary surface.



## -parameters




### -param arg1 [in]

Flag that indicates whether gamma calibration is required. Set this parameter to DDSGR_CALIBRATE to request that the calibrator adjust the gamma ramp according to the physical properties of the display, which makes the result identical on all computers. If calibration is not needed, set this parameter to 0.


### -param arg2 [in]

A pointer to a <a href="https://msdn.microsoft.com/ec4cb111-3b12-4470-b1e3-e4379f7f2632">DDGAMMARAMP</a> structure that contains the new red, green, and blue gamma ramp entries. Each array maps color values in the frame buffer to the color values to be passed to the digital-to-analog converter (DAC).


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



Not all systems support gamma calibration. To determine whether gamma calibration is supported, call <a href="https://msdn.microsoft.com/4e93612c-9e28-4d51-a640-e8e9b5ed8e7a">IDirectDraw7::GetCaps</a> and examine the <b>dwCaps2</b> member of the associated <a href="https://msdn.microsoft.com/4ddda0a7-c0db-47cf-a908-959aabb530c6">DDCAPS</a> structure after the method returns. If the DDCAPS2_CANCALIBRATEGAMMA capability flag is present, gamma calibration is supported.



Calibrating gamma ramps incurs some processing overhead and should not be used frequently.

Including the DDSGR_CALIBRATE flag in the <i>dwFlags</i> parameter when running on computers that do not support gamma calibration does not cause this method to fail. The method succeeds and sets new gamma ramp values without calibration.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetGammaRamp</b> method.




## -see-also




<a href="https://msdn.microsoft.com/a6286a2d-76d5-49ec-afd5-cbf112528db8">IDirectDrawGammaControl</a>
 

 

