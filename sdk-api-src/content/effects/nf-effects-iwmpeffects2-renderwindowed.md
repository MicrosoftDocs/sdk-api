---
UID: NF:effects.IWMPEffects2.RenderWindowed
title: IWMPEffects2::RenderWindowed method
author: windows-driver-content
description: The RenderWindowed method is called by Windows Media Player to render a windowed visualization.
old-location: wmp\iwmpeffects2_renderwindowed.htm
old-project: WMP
ms.assetid: 95a0b71e-6485-4b14-81cf-b853a664b3cc
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPEffects2, IWMPEffects2 interface [Windows Media Player], RenderWindowed method, IWMPEffects2::RenderWindowed, IWMPEffectsRenderWindowed, RenderWindowed method [Windows Media Player], RenderWindowed method [Windows Media Player], IWMPEffects2 interface, RenderWindowed,IWMPEffects2.RenderWindowed, effects/IWMPEffects2::RenderWindowed, wmp.iwmpeffects2_renderwindowed
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	effects.h
api_name:
-	IWMPEffects2.RenderWindowed
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IWMPEffects2::RenderWindowed method


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




<a href="https://msdn.microsoft.com/44e044c1-97fd-43cb-9530-4556e485f5ae">IWMPEffects2 Interface</a>



<a href="https://msdn.microsoft.com/9040c309-5e45-41d2-9a02-b17c6d764f59">IWMPEffects::Render</a>



<a href="https://msdn.microsoft.com/a33d4cd1-e888-4ecd-9e6c-113febfefd99">TimedLevel</a>
 

 

