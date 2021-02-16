---
UID: NS:ddraw._DDGAMMARAMP
title: DDGAMMARAMP (ddraw.h)
description: The DDGAMMARAMP structure contains red, green, and blue ramp data for the IDirectDrawGammaControl::GetGammaRamp and IDirectDrawGammaControl::SetGammaRamp methods.
helpviewer_keywords: ["*LPDDGAMMARAMP","DDGAMMARAMP","DDGAMMARAMP structure [DirectDraw]","LPDDGAMMARAMP","LPDDGAMMARAMP structure pointer [DirectDraw]","ddraw/DDGAMMARAMP","ddraw/LPDDGAMMARAMP","directdraw.ddgammaramp"]
old-location: directdraw\ddgammaramp.htm
tech.root: directdraw
ms.assetid: ec4cb111-3b12-4470-b1e3-e4379f7f2632
ms.date: 12/05/2018
ms.keywords: '*LPDDGAMMARAMP, DDGAMMARAMP, DDGAMMARAMP structure [DirectDraw], LPDDGAMMARAMP, LPDDGAMMARAMP structure pointer [DirectDraw], ddraw/DDGAMMARAMP, ddraw/LPDDGAMMARAMP, directdraw.ddgammaramp'
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
targetos: Windows
req.typenames: DDGAMMARAMP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGAMMARAMP
 - ddraw/_DDGAMMARAMP
 - DDGAMMARAMP
 - ddraw/DDGAMMARAMP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddraw.h
api_name:
 - DDGAMMARAMP
---

# DDGAMMARAMP structure


## -description

The <b>DDGAMMARAMP</b> structure contains red, green, and blue ramp data for the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawgammacontrol-getgammaramp">IDirectDrawGammaControl::GetGammaRamp</a> and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawgammacontrol-setgammaramp">IDirectDrawGammaControl::SetGammaRamp</a> methods.

## -struct-fields

### -field red

Array of 256 WORD elements that describe the red gamma ramp.

### -field green

Array of 256 WORD elements that describe the green gamma ramp.

### -field blue

Array of 256 WORD elements that describe the blue gamma ramp.