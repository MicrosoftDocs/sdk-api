---
UID: NF:effects.IWMPEffects.Render
title: IWMPEffects::Render
author: windows-sdk-content
description: The Render method renders the visualization.
old-location: wmp\iwmpeffects_render.htm
tech.root: WMP
ms.assetid: 9040c309-5e45-41d2-9a02-b17c6d764f59
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EffectsRender, IWMPEffects interface [Windows Media Player],Render method, IWMPEffects.Render, IWMPEffects::Render, Render, Render method [Windows Media Player], Render method [Windows Media Player],IWMPEffects interface, effects/IWMPEffects::Render, wmp.iwmpeffects_render
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
 - IWMPEffects.Render
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEffects::Render


## -description



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




<a href="https://msdn.microsoft.com/en-us/library/Dd563253(v=VS.85).aspx">IWMPEffects Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd564504(v=VS.85).aspx">TimedLevel</a>
 

 

