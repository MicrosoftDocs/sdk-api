---
UID: NF:rtscom.IDynamicRenderer.Draw
title: IDynamicRenderer::Draw
author: windows-sdk-content
description: Draws the cached data to the specified device context.
old-location: tablet\idynamicrenderer_draw.htm
tech.root: tablet
ms.assetid: d0f05fc7-2b54-40fc-823a-dad0a86174d6
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: Draw, Draw method [Tablet PC], Draw method [Tablet PC],IDynamicRenderer interface, IDynamicRenderer interface [Tablet PC],Draw method, IDynamicRenderer.Draw, IDynamicRenderer::Draw, d0f05fc7-2b54-40fc-823a-dad0a86174d6, rtscom/IDynamicRenderer::Draw, tablet.idynamicrenderer_draw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IDynamicRenderer.Draw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDynamicRenderer::Draw


## -description



Draws the cached data to the specified device context.




## -parameters




### -param hDC [in]

 The handle of the device context on which to draw.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



You can use <b>IDynamicRenderer::Draw Method</b> for tasks such as double buffering.

<div class="alert"><b>Note</b>  Drawing cached data cannot be used on Microsoft&lt;entity type="reg"/&gt; Windows&lt;entity type="reg"/&gt; XP Tablet PC Edition 2005 systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6435b297-d6a7-418b-afc0-f8cc0b329842">IDynamicRenderer Interface</a>



<a href="https://msdn.microsoft.com/1b2435ee-4682-4499-aa5c-35201ab2ba95">IDynamicRenderer::DataCacheEnabled Property</a>



<a href="https://msdn.microsoft.com/d67a85e7-6dfc-4444-bb69-a46e1234d021">IDynamicRenderer::DrawingAttributes Property</a>



<a href="https://msdn.microsoft.com/691de815-a5be-4982-a59a-b904c070ede8">IDynamicRenderer::ReleaseCachedData Method</a>
 

 

