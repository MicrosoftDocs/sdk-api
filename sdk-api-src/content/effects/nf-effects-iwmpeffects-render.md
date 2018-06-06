---
UID: NF:effects.IWMPEffects.Render
title: IWMPEffects::Render
author: windows-sdk-content
description: The Render method renders the visualization.
old-location: wmp\iwmpeffects_render.htm
old-project: WMP
ms.assetid: 9040c309-5e45-41d2-9a02-b17c6d764f59
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: EffectsRender, IWMPEffects interface [Windows Media Player],Render method, IWMPEffects.Render, IWMPEffects::Render, Render, Render method [Windows Media Player], Render method [Windows Media Player],IWMPEffects interface, effects/IWMPEffects::Render, wmp.iwmpeffects_render
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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




<a href="https://msdn.microsoft.com/0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba">IWMPEffects Interface</a>



<a href="https://msdn.microsoft.com/a33d4cd1-e888-4ecd-9e6c-113febfefd99">TimedLevel</a>
 

 

