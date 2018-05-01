---
UID: NF:ddrawgdi.DdSetGammaRamp
title: DdSetGammaRamp function
author: windows-driver-content
description: The DdSetGammaRamp function sets the gamma ramp for the device.
old-location: winprog\_dxgkernel_ddsetgammaramp.htm
old-project: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddsetgammaramp.htm
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: DdSetGammaRamp, DdSetGammaRamp function [Windows API], GdiEntry15, _dxgkernel_ddsetgammaramp, ddrawgdi/DdSetGammaRamp, ddrawgdi/GdiEntry15, winprog._dxgkernel_ddsetgammaramp, winui._dxgkernel_ddsetgammaramp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ddrawgdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: "*LPDDSURFACEDESC2, DDSURFACEDESC2"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ddrawgdi.h
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32.dll
-	GDI32Full.dll
api_name:
-	DdSetGammaRamp
-	GdiEntry15
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DdSetGammaRamp function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

The <b>DdSetGammaRamp</b> function sets the gamma ramp for the device.

<b>GdiEntry15</b> is defined as an alias for this function.


## -parameters




### -param pDDraw [in]

Pointer to user-mode DirectDraw device object.


### -param hdc [in]

Reserved.


### -param lpGammaRamp [in]

Pointer to an array of <b>DDGAMMARAMP</b> structures.


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>NULL</b>.




## -remarks



It is recommended that applications use the <b>IDirectDrawGammaControl::SetGammaRamp</b> or <b>IDirect3DDevice9::SetGammaRamp</b> methods instead since these methods offer the same functionality independent of the operating system.




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

