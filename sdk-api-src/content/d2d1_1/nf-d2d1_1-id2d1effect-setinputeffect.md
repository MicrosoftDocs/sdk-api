---
UID: NF:d2d1_1.ID2D1Effect.SetInputEffect
title: ID2D1Effect::SetInputEffect
author: windows-sdk-content
description: Sets the given input effect by index.
old-location: direct2d\id2d1effect_setinputeffect.htm
tech.root: direct2d
ms.assetid: 361B0644-7437-47DA-A34C-0234EE4E92C3
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ID2D1Effect interface [Direct2D],SetInputEffect method, ID2D1Effect.SetInputEffect, ID2D1Effect::SetInputEffect, SetInputEffect, SetInputEffect method [Direct2D], SetInputEffect method [Direct2D],ID2D1Effect interface, d2d1_1/ID2D1Effect::SetInputEffect, direct2d.id2d1effect_setinputeffect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Effect.SetInputEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Effect::SetInputEffect


## -description


Sets the given input effect by index. 

This method gets the output of the given effect and then passes the output image to the <a href="https://msdn.microsoft.com/16db95e8-43e7-403c-bce1-dd2f42e81d6a">SetInput</a> method.


## -parameters




### -param index

The index of the input to set.


### -param inputEffect

TBD


### -param invalidate

Whether to invalidate the graph at the location of the effect input


#### - input [in, optional]

The input effect to set.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>



<a href="https://msdn.microsoft.com/e14066f7-b195-44f1-a952-1b6c9f3832cf">ID2D1Effect::GetOutput</a>



<a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>
 

 

