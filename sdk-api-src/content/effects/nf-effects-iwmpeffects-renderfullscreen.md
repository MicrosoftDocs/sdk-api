---
UID: NF:effects.IWMPEffects.RenderFullScreen
title: IWMPEffects::RenderFullScreen (effects.h)
description: The RenderFullScreen method renders the visualization in full-screen mode.
helpviewer_keywords: ["EffectsRenderFullScreen","IWMPEffects interface [Windows Media Player]","RenderFullScreen method","IWMPEffects.RenderFullScreen","IWMPEffects::RenderFullScreen","RenderFullScreen","RenderFullScreen method [Windows Media Player]","RenderFullScreen method [Windows Media Player]","IWMPEffects interface","effects/IWMPEffects::RenderFullScreen","wmp.iwmpeffects_renderfullscreen"]
old-location: wmp\iwmpeffects_renderfullscreen.htm
tech.root: WMP
ms.assetid: 08b170fd-b40a-4beb-8c18-0a011b9486af
ms.date: 12/05/2018
ms.keywords: EffectsRenderFullScreen, IWMPEffects interface [Windows Media Player],RenderFullScreen method, IWMPEffects.RenderFullScreen, IWMPEffects::RenderFullScreen, RenderFullScreen, RenderFullScreen method [Windows Media Player], RenderFullScreen method [Windows Media Player],IWMPEffects interface, effects/IWMPEffects::RenderFullScreen, wmp.iwmpeffects_renderfullscreen
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player version 7.0 or later.
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEffects::RenderFullScreen
 - effects/IWMPEffects::RenderFullScreen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - effects.h
api_name:
 - IWMPEffects.RenderFullScreen
---

# IWMPEffects::RenderFullScreen


## -description

The <b>RenderFullScreen</b> method renders the visualization in full-screen mode.

## -parameters

### -param pLevels [in]

Pointer to a <b>TimedLevel</b> structure.

## -returns

If the method succeeds, your implementation should return S_OK. If it fails, return an <b>HRESULT</b> error code.

## -remarks

The <b>GoFullscreen</b> method must be called with a <b>True</b> value before <b>RenderFullScreen</b> can be called.

The user can enter or leave full screen mode by pressing the Alt and Enter keys simultaneously.

A default implementation of this method is not included in the visualization wizard.

If your implementation returns an error from this method, then <b>GoFullscreen</b>(<b>False</b>) will be called to ask your visualization to drop out of full screen mode.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>



<a href="/previous-versions/windows/desktop/api/effects/ns-effects-timedlevel">TimedLevel</a>