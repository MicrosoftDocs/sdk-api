---
UID: NF:effects.IWMPEffects2.RenderWindowed
title: IWMPEffects2::RenderWindowed (effects.h)
description: The RenderWindowed method is called by Windows Media Player to render a windowed visualization.helpviewer_keywords: ["IWMPEffects2 interface [Windows Media Player]","RenderWindowed method","IWMPEffects2.RenderWindowed","IWMPEffects2::RenderWindowed","IWMPEffectsRenderWindowed","RenderWindowed","RenderWindowed method [Windows Media Player]","RenderWindowed method [Windows Media Player]","IWMPEffects2 interface","effects/IWMPEffects2::RenderWindowed","wmp.iwmpeffects2_renderwindowed"]
old-location: wmp\iwmpeffects2_renderwindowed.htm
tech.root: WMP
ms.assetid: 95a0b71e-6485-4b14-81cf-b853a664b3cc
ms.date: 12/05/2018
ms.keywords: IWMPEffects2 interface [Windows Media Player],RenderWindowed method, IWMPEffects2.RenderWindowed, IWMPEffects2::RenderWindowed, IWMPEffectsRenderWindowed, RenderWindowed, RenderWindowed method [Windows Media Player], RenderWindowed method [Windows Media Player],IWMPEffects2 interface, effects/IWMPEffects2::RenderWindowed, wmp.iwmpeffects2_renderwindowed
f1_keywords:
- effects/IWMPEffects2.RenderWindowed
dev_langs:
- c++
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
- COM
api_location:
- effects.h
api_name:
- IWMPEffects2.RenderWindowed
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEffects2::RenderWindowed


## -description



The <b>RenderWindowed</b> method is called by Windows Media Player to render a windowed visualization.




## -parameters




### -param pData [in]

Pointer to a <b>TimedLevel</b> structure specifying rendering information.


### -param fRequiredRender [in]

<b>BOOL</b> indicating whether the visualization must paint itself.


## -returns



This method returns an <b>HRESULT</b>.




## -remarks



This method is used to render windowed visualizations. Windowless visualizations should return S_OK and use the <b>IWMPEffects::Render</b> method instead.

The <i>fRequiredRender</i> parameter informs you that your visualization must repaint itself, for example, when another window is dragged over it. When this value is false, you can safely skip over the rendering code if the current media item is stopped or paused. This lets you avoid consuming CPU cycles unnecessarily.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/effects/nn-effects-iwmpeffects2">IWMPEffects2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-render">IWMPEffects::Render</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/effects/ns-effects-timedlevel">TimedLevel</a>
 

 

