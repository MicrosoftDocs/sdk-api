---
UID: NF:ddraw.IDirectDrawGammaControl.GetGammaRamp
title: IDirectDrawGammaControl::GetGammaRamp
author: windows-sdk-content
description: Retrieves the red, green, and blue gamma ramps for the primary surface.
old-location: directdraw\idirectdrawgammacontrol_getgammaramp.htm
tech.root: directdraw
ms.assetid: ba83605c-c388-42c0-9297-1666c80a278e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetGammaRamp, GetGammaRamp method [DirectDraw], GetGammaRamp method [DirectDraw],IDirectDrawGammaControl interface, IDirectDrawGammaControl interface [DirectDraw],GetGammaRamp method, IDirectDrawGammaControl.GetGammaRamp, IDirectDrawGammaControl::GetGammaRamp, ddraw/IDirectDrawGammaControl::GetGammaRamp, directdraw.idirectdrawgammacontrol_getgammaramp
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirectDrawGammaControl.GetGammaRamp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawGammaControl::GetGammaRamp


## -description


Retrieves the red, green, and blue gamma ramps for the primary surface.


## -parameters




### -param arg1

TBD


### -param arg2

TBD




#### - dwFlags [in]

Currently not used and must be set to 0.


#### - lpRampData [in, out]

A pointer to a <a href="https://msdn.microsoft.com/ec4cb111-3b12-4470-b1e3-e4379f7f2632">DDGAMMARAMP</a> structure that receives the current red, green, and blue gamma ramps. Each array maps color values in the frame buffer to the color values to be passed to the digital-to-analog converter (DAC).


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXCEPTION</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetGammaRamp</b> method.




## -see-also




<a href="https://msdn.microsoft.com/a6286a2d-76d5-49ec-afd5-cbf112528db8">IDirectDrawGammaControl</a>
 

 

