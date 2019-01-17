---
UID: NF:d2d1_1.ID2D1Effect.GetInput
title: ID2D1Effect::GetInput
author: windows-sdk-content
description: Gets the given input image by index.
old-location: direct2d\id2d1effect_getinput.htm
tech.root: Direct2D
ms.assetid: fca22cc2-2299-4f74-8dc9-d931b899d4fb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInput, GetInput method [Direct2D], GetInput method [Direct2D],ID2D1Effect interface, ID2D1Effect interface [Direct2D],GetInput method, ID2D1Effect.GetInput, ID2D1Effect::GetInput, d2d1_1/ID2D1Effect::GetInput, direct2d.id2d1effect_getinput
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
 - ID2D1Effect.GetInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Effect::GetInput


## -description


Gets the given input image by index. 


## -parameters




### -param index

Type: <b>UINT32</b>

The index of the image to retrieve.


### -param input [out, optional]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>**</b>

When this method returns, contains the address of a pointer to the image that is identified by <i>Index</i>.


## -returns



This method does not return a value.




## -remarks



If the input index is out of range, the returned image will be <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">ID2D1DeviceContext::DrawImage</a>



<a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>



<a href="https://msdn.microsoft.com/e14066f7-b195-44f1-a952-1b6c9f3832cf">ID2D1Effect::GetOutput</a>



<a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>
 

 

