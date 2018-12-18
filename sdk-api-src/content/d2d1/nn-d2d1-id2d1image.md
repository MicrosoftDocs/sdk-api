---
UID: NN:d2d1.ID2D1Image
title: ID2D1Image
author: windows-sdk-content
description: Represents a producer of pixels that can fill an arbitrary 2D plane.
old-location: direct2d\id2d1image.htm
tech.root: direct2d
ms.assetid: 9f7b4546-edbe-4000-a4ce-1a69563ebf9d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1Image, ID2D1Image interface [Direct2D], ID2D1Image interface [Direct2D],described, d2d1/ID2D1Image, direct2d.id2d1image
ms.topic: interface
req.header: d2d1.h
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
 - ID2D1Image
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Image interface


## -description


Represents a producer of pixels that can fill an arbitrary 2D plane.


## -remarks



An <b>ID2D1Image</b> is abstract.  Concrete instances can be created through <a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a> and <a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">ID2D1DeviceContext::CreateBitmap</a>.

Images are evaluated lazily. If the type of image passed in is concrete, then the image can be directly sampled from. Other images can act only as a source of pixels and can produce content only as a result of calling <a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">ID2D1DeviceContext::DrawImage</a>.




## -see-also




<a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>



<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>



<a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a>
 

 

