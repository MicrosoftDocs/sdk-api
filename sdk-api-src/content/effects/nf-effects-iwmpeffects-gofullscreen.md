---
UID: NF:effects.IWMPEffects.GoFullscreen
title: IWMPEffects::GoFullscreen (effects.h)
description: The GoFullscreen method instructs the visualization to switch to full-screen mode.
helpviewer_keywords: ["EffectsGoFullscreen","GoFullscreen","GoFullscreen method [Windows Media Player]","GoFullscreen method [Windows Media Player]","IWMPEffects interface","IWMPEffects interface [Windows Media Player]","GoFullscreen method","IWMPEffects.GoFullscreen","IWMPEffects::GoFullscreen","effects/IWMPEffects::GoFullscreen","wmp.iwmpeffects_gofullscreen"]
old-location: wmp\iwmpeffects_gofullscreen.htm
tech.root: WMP
ms.assetid: daf69206-5756-4504-9738-e16b9af39790
ms.date: 12/05/2018
ms.keywords: EffectsGoFullscreen, GoFullscreen, GoFullscreen method [Windows Media Player], GoFullscreen method [Windows Media Player],IWMPEffects interface, IWMPEffects interface [Windows Media Player],GoFullscreen method, IWMPEffects.GoFullscreen, IWMPEffects::GoFullscreen, effects/IWMPEffects::GoFullscreen, wmp.iwmpeffects_gofullscreen
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
 - IWMPEffects::GoFullscreen
 - effects/IWMPEffects::GoFullscreen
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
 - IWMPEffects.GoFullscreen
---

# IWMPEffects::GoFullscreen


## -description

The <b>GoFullscreen</b> method instructs the visualization to switch to full-screen mode.

## -parameters

### -param fFullScreen [in]

<b>Boolean</b> indicating whether to switch to full-screen mode.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called when the visualization is to go full screen or leave full screen. If the full screen capabilities flag is not returned through <b>GetCapabilities</b>, your visualization will not be asked to go or render full screen. This method will be called before <b>RenderFullScreen</b> is called.

A default implementation of this method is not included in the visualization wizard.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>