---
UID: NF:effects.IWMPEffects.RenderFullScreen
title: IWMPEffects::RenderFullScreen
author: windows-sdk-content
description: The RenderFullScreen method renders the visualization in full-screen mode.
old-location: wmp\iwmpeffects_renderfullscreen.htm
tech.root: WMP
ms.assetid: 08b170fd-b40a-4beb-8c18-0a011b9486af
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: EffectsRenderFullScreen, IWMPEffects interface [Windows Media Player],RenderFullScreen method, IWMPEffects.RenderFullScreen, IWMPEffects::RenderFullScreen, RenderFullScreen, RenderFullScreen method [Windows Media Player], RenderFullScreen method [Windows Media Player],IWMPEffects interface, effects/IWMPEffects::RenderFullScreen, wmp.iwmpeffects_renderfullscreen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - effects.h
api_name:
 - IWMPEffects.RenderFullScreen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba">IWMPEffects Interface</a>



<a href="https://msdn.microsoft.com/a33d4cd1-e888-4ecd-9e6c-113febfefd99">TimedLevel</a>
 

 

