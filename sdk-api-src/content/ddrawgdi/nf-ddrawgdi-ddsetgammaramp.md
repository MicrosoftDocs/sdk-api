---
UID: NF:ddrawgdi.DdSetGammaRamp
title: DdSetGammaRamp function (ddrawgdi.h)
description: The DdSetGammaRamp function sets the gamma ramp for the device.
helpviewer_keywords: ["DdSetGammaRamp","DdSetGammaRamp function [Windows API]","GdiEntry15","_dxgkernel_ddsetgammaramp","ddrawgdi/DdSetGammaRamp","ddrawgdi/GdiEntry15","winprog._dxgkernel_ddsetgammaramp","winui._dxgkernel_ddsetgammaramp"]
old-location: winprog\_dxgkernel_ddsetgammaramp.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddsetgammaramp.htm
ms.date: 12/05/2018
ms.keywords: DdSetGammaRamp, DdSetGammaRamp function [Windows API], GdiEntry15, _dxgkernel_ddsetgammaramp, ddrawgdi/DdSetGammaRamp, ddrawgdi/GdiEntry15, winprog._dxgkernel_ddsetgammaramp, winui._dxgkernel_ddsetgammaramp
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdSetGammaRamp
 - ddrawgdi/DdSetGammaRamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ddrawgdi.h
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - DdSetGammaRamp
 - GdiEntry15
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

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>