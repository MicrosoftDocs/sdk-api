---
UID: NS:ddraw._DDGAMMARAMP
title: "_DDGAMMARAMP"
author: windows-sdk-content
description: The DDGAMMARAMP structure contains red, green, and blue ramp data for the IDirectDrawGammaControl::GetGammaRamp and IDirectDrawGammaControl::SetGammaRamp methods.
old-location: directdraw\ddgammaramp.htm
tech.root: directdraw
ms.assetid: ec4cb111-3b12-4470-b1e3-e4379f7f2632
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPDDGAMMARAMP, DDGAMMARAMP, DDGAMMARAMP structure [DirectDraw], LPDDGAMMARAMP, LPDDGAMMARAMP structure pointer [DirectDraw], _DDGAMMARAMP, ddraw/DDGAMMARAMP, ddraw/LPDDGAMMARAMP, directdraw.ddgammaramp"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddraw.h
api_name:
 - DDGAMMARAMP
product: Windows
targetos: Windows
req.typenames: DDGAMMARAMP
req.redist: 
---

# _DDGAMMARAMP structure


## -description


The <b>DDGAMMARAMP</b> structure contains red, green, and blue ramp data for the <a href="https://msdn.microsoft.com/ba83605c-c388-42c0-9297-1666c80a278e">IDirectDrawGammaControl::GetGammaRamp</a> and <a href="https://msdn.microsoft.com/3bde7ba7-8498-42e5-bd5a-625e162fc1db">IDirectDrawGammaControl::SetGammaRamp</a> methods.




## -struct-fields




### -field red

Array of 256 WORD elements that describe the red gamma ramp.


### -field green

Array of 256 WORD elements that describe the green gamma ramp.


### -field blue

Array of 256 WORD elements that describe the blue gamma ramp.

