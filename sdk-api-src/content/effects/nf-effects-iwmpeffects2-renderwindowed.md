---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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




<a href="https://msdn.microsoft.com/44e044c1-97fd-43cb-9530-4556e485f5ae">IWMPEffects2 Interface</a>



<a href="https://msdn.microsoft.com/9040c309-5e45-41d2-9a02-b17c6d764f59">IWMPEffects::Render</a>



<a href="https://msdn.microsoft.com/a33d4cd1-e888-4ecd-9e6c-113febfefd99">TimedLevel</a>
 

 

