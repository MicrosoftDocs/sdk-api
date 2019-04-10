---
UID: NF:d2d1_1.ID2D1Effect.SetInput
title: ID2D1Effect::SetInput (d2d1_1.h)
author: windows-sdk-content
description: Sets the given input image by index.
old-location: direct2d\id2d1effect_setinput.htm
tech.root: Direct2D
ms.assetid: 16db95e8-43e7-403c-bce1-dd2f42e81d6a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1Effect interface [Direct2D],SetInput method, ID2D1Effect.SetInput, ID2D1Effect::SetInput, SetInput, SetInput method [Direct2D], SetInput method [Direct2D],ID2D1Effect interface, d2d1_1/ID2D1Effect::SetInput, direct2d.id2d1effect_setinput
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
 - ID2D1Effect.SetInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Effect::SetInput


## -description


Sets the given input image by index. 


## -parameters




### -param index

Type: <b>UINT32</b>

The index of the image to set.


### -param input [in, optional]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>*</b>

The input image to set.


### -param invalidate

Type: <b>BOOL</b>

Whether to invalidate the graph at the location of the effect input


## -returns



This method does not return a value.




## -remarks



If the input index is out of range, the input image is ignored. 




## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>



<a href="https://msdn.microsoft.com/e14066f7-b195-44f1-a952-1b6c9f3832cf">ID2D1Effect::GetOutput</a>



<a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>
 

 

