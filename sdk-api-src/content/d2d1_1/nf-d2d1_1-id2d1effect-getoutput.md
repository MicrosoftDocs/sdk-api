---
UID: NF:d2d1_1.ID2D1Effect.GetOutput
title: ID2D1Effect::GetOutput
author: windows-sdk-content
description: Gets the output image from the effect.
old-location: direct2d\id2d1effect_getoutput.htm
old-project: direct2d
ms.assetid: e14066f7-b195-44f1-a952-1b6c9f3832cf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetOutput, GetOutput method [Direct2D], GetOutput method [Direct2D],ID2D1Effect interface, ID2D1Effect interface [Direct2D],GetOutput method, ID2D1Effect.GetOutput, ID2D1Effect::GetOutput, d2d1_1/ID2D1Effect::GetOutput, direct2d.id2d1effect_getoutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_UNIT_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Effect.GetOutput
product: Windows
targetos: Windows
req.lib: 
req.dll: D2d1.dll
req.irql: 
---

# ID2D1Effect::GetOutput


## -description


Gets the output image from the effect. 


## -parameters




### -param outputImage [out]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>**</b>

When this method returns, contains the address of a pointer to the output image for the effect.


## -returns



This method does not return a value.




## -remarks



The output image  can be set as an input to another effect, or can be directly passed into the <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a> in order to render the effect. 

It is  also possible to use <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to retrieve the same output image.




## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">ID2D1DeviceContext::DrawImage</a>



<a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>



<a href="https://msdn.microsoft.com/e14066f7-b195-44f1-a952-1b6c9f3832cf">ID2D1Effect::GetOutput</a>



<a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>
 

 

