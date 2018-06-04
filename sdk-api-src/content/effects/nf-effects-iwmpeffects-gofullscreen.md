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

# IWMPEffects::GoFullscreen


## -description



The <b>GoFullscreen</b> method instructs the visualization to switch to full-screen mode.




## -parameters




### -param fFullScreen






#### - fFullscreen [in]

<b>Boolean</b> indicating whether to switch to full-screen mode.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method is called when the visualization is to go full screen or leave full screen. If the full screen capabilities flag is not returned through <b>GetCapabilities</b>, your visualization will not be asked to go or render full screen. This method will be called before <b>RenderFullScreen</b> is called.

A default implementation of this method is not included in the visualization wizard.




## -see-also




<a href="https://msdn.microsoft.com/0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba">IWMPEffects Interface</a>
 

 

