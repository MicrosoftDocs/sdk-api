---
UID: NF:rtscom.IDynamicRenderer.Refresh
title: IDynamicRenderer::Refresh (rtscom.h)
author: windows-sdk-content
description: Causes the DynamicRenderer Class object to redraw the ink data that is currently rendering.
old-location: tablet\idynamicrenderer_refresh.htm
tech.root: tablet
ms.assetid: 409d4353-fc85-49ff-99a4-d8393a3c0ec4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 409d4353-fc85-49ff-99a4-d8393a3c0ec4, IDynamicRenderer interface [Tablet PC],Refresh method, IDynamicRenderer.Refresh, IDynamicRenderer::Refresh, Refresh, Refresh method [Tablet PC], Refresh method [Tablet PC],IDynamicRenderer interface, rtscom/IDynamicRenderer::Refresh, tablet.idynamicrenderer_refresh
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
 - IDynamicRenderer.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDynamicRenderer::Refresh


## -description



Causes the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object to redraw the ink data that is currently rendering.




## -parameters






## -returns



This method can return one of these values.




## -remarks



If the <a href="https://msdn.microsoft.com/1b2435ee-4682-4499-aa5c-35201ab2ba95">IDynamicRenderer::DataCacheEnabled Property</a> property is <b>true</b>, then the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object redraws all tablet stylus data not yet released from the cache. If the <b>IDynamicRenderer::DataCacheEnabled Property</b> property is <b>false</b>, then the <b>DynamicRenderer Class</b> object redraws only the current stroke.

When calling the <b>IDynamicRenderer::Refresh Method</b> from within a Paint event handler, set the <a href="https://msdn.microsoft.com/0d3c6d2e-1675-4335-a283-ea14a818469a">IDynamicRenderer::ClipRectangle Property</a> to the Paint event's rectangle.




## -see-also




<a href="https://msdn.microsoft.com/d0f05fc7-2b54-40fc-823a-dad0a86174d6">Draw Method</a>



<a href="https://msdn.microsoft.com/6435b297-d6a7-418b-afc0-f8cc0b329842">IDynamicRenderer Interface</a>



<a href="https://msdn.microsoft.com/d67a85e7-6dfc-4444-bb69-a46e1234d021">IDynamicRenderer::DrawingAttributes Property</a>
 

 

