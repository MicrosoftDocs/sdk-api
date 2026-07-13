---
UID: NF:effects.IWMPEffects.Render
title: IWMPEffects::Render (effects.h)
description: The Render method renders the visualization.
helpviewer_keywords: ["EffectsRender","IWMPEffects interface [Windows Media Player]","Render method","IWMPEffects.Render","IWMPEffects::Render","Render","Render method [Windows Media Player]","Render method [Windows Media Player]","IWMPEffects interface","effects/IWMPEffects::Render","wmp.iwmpeffects_render"]
old-location: wmp\iwmpeffects_render.htm
tech.root: WMP
ms.assetid: 9040c309-5e45-41d2-9a02-b17c6d764f59
ms.date: 4/26/2023
ms.keywords: EffectsRender, IWMPEffects interface [Windows Media Player],Render method, IWMPEffects.Render, IWMPEffects::Render, Render, Render method [Windows Media Player], Render method [Windows Media Player],IWMPEffects interface, effects/IWMPEffects::Render, wmp.iwmpeffects_render
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
 - IWMPEffects::Render
 - effects/IWMPEffects::Render
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
 - IWMPEffects.Render
---

# IWMPEffects::Render


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Render</b> method renders the visualization.

## -parameters

### -param pLevels [in]

Pointer to a <b>TimedLevel</b> structure.

### -param hdc [in]

Specifies a handle to a device context.

### -param prc [in]

Specifies the rectangle the visualization is to be rendered in.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The device context is normalized by this method.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>



<a href="/previous-versions/windows/desktop/api/effects/ns-effects-timedlevel">TimedLevel</a>