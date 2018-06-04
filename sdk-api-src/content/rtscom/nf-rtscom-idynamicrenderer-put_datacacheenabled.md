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

# IDynamicRenderer::put_DataCacheEnabled


## -description



Gets or sets a value that indicates whether data caching is enabled for the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object.



This property is read/write.


## -parameters


## -remarks



Setting the <b>DataCacheEnabled</b> property to <b>TRUE</b> enables you to manage the situation where slow processes block the output queue. When the window is invalidated after strokes are drawn by the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object, there may be a delay before the collected strokes are drawn. Place the strokes of the dynamic renderer in a cache and use the <a href="https://msdn.microsoft.com/409d4353-fc85-49ff-99a4-d8393a3c0ec4">IDynamicRenderer::Refresh Method</a> method to redraw the strokes.

After the strokes are collected, you must release them from the cache by calling the <a href="https://msdn.microsoft.com/691de815-a5be-4982-a59a-b904c070ede8">IDynamicRenderer::ReleaseCachedData Method</a> method. Use the <a href="https://msdn.microsoft.com/0d3f556c-b0a8-4346-b7da-82f1a3c2603c">IStylusPlugin::CustomStylusDataAdded Method</a> method to release the strokes.

It is also useful to set the <b>DataCacheEnabled</b> property to <b>TRUE</b> when you want to display strokes as they are drawn, but have no need to store the strokes after you have done something with them. In this case, store the data identifiers in the data parameter of the <a href="https://msdn.microsoft.com/0d3f556c-b0a8-4346-b7da-82f1a3c2603c">IStylusPlugin::CustomStylusDataAdded Method</a> method, and then release the data when you no longer need the cached strokes.

If this property is <b>TRUE</b>, you must call the <a href="https://msdn.microsoft.com/691de815-a5be-4982-a59a-b904c070ede8">IDynamicRenderer::ReleaseCachedData Method</a> method for strokes which have been stored in the ink collecting object. If <b>FALSE</b>, you are not required to call the <b>IDynamicRenderer::ReleaseCachedData Method</b> method. The disadvantage to setting this property to <b>FALSE</b> is that any stroke data that was initially dynamically rendered but invalidated by other miscellaneous operations does not render until the stroke data reaches the ink collection object and is rendered there.

Setting this property to <b>FALSE</b> clears the cached data.




## -see-also




<a href="https://msdn.microsoft.com/6435b297-d6a7-418b-afc0-f8cc0b329842">IDynamicRenderer Interface</a>



<a href="https://msdn.microsoft.com/691de815-a5be-4982-a59a-b904c070ede8">IDynamicRenderer::ReleaseCachedData Method</a>
 

 

