---
UID: NF:rtscom.IDynamicRenderer.ReleaseCachedData
title: IDynamicRenderer::ReleaseCachedData (rtscom.h)
author: windows-sdk-content
description: Releases specified stroke data from the temporal data held by DynamicRenderer Class.
old-location: tablet\idynamicrenderer_releasecacheddata.htm
tech.root: tablet
ms.assetid: 691de815-a5be-4982-a59a-b904c070ede8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 691de815-a5be-4982-a59a-b904c070ede8, IDynamicRenderer interface [Tablet PC],ReleaseCachedData method, IDynamicRenderer.ReleaseCachedData, IDynamicRenderer::ReleaseCachedData, ReleaseCachedData, ReleaseCachedData method [Tablet PC], ReleaseCachedData method [Tablet PC],IDynamicRenderer interface, rtscom/IDynamicRenderer::ReleaseCachedData, tablet.idynamicrenderer_releasecacheddata
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
 - IDynamicRenderer.ReleaseCachedData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDynamicRenderer::ReleaseCachedData


## -description



Releases specified stroke data from the temporal data held by <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>.




## -parameters




### -param strokeId

The identifier for the stroke.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



This method is used only when the <a href="https://msdn.microsoft.com/1b2435ee-4682-4499-aa5c-35201ab2ba95">IDynamicRenderer::DataCacheEnabled Property</a> property is set to <b>true</b>.

The <b>IDynamicRenderer::ReleaseCachedData Method</b> method enables you to release the specified stroke data from the temporal data held by the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object.


<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> strokes can be placed in a cache, so they can be redrawn by calling the <a href="https://msdn.microsoft.com/409d4353-fc85-49ff-99a4-d8393a3c0ec4">IDynamicRenderer::Refresh Method</a> method. After the strokes are collected, release them from the cache by calling the <b>IDynamicRenderer::ReleaseCachedData Method</b> method. Generally, the release occurs in the <a href="https://msdn.microsoft.com/0d3f556c-b0a8-4346-b7da-82f1a3c2603c">IStylusPlugin::CustomStylusDataAdded Method</a> method.

<i>strokeId</i> cannot accept a value of less than zero. 




## -see-also




<a href="https://msdn.microsoft.com/d0f05fc7-2b54-40fc-823a-dad0a86174d6">Draw Method</a>



<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/6435b297-d6a7-418b-afc0-f8cc0b329842">IDynamicRenderer Interface</a>
 

 

