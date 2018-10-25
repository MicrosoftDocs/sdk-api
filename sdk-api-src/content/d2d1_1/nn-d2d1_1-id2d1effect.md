---
UID: NN:d2d1_1.ID2D1Effect
title: ID2D1Effect
author: windows-sdk-content
description: Represents a basic image-processing construct in Direct2D.
old-location: direct2d\id2d1effect.htm
tech.root: direct2d
ms.assetid: e90d1830-c356-48f1-ac7b-1d94c8c26569
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ID2D1Effect, ID2D1Effect interface [Direct2D], ID2D1Effect interface [Direct2D],described, d2d1_1/ID2D1Effect, direct2d.id2d1effect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ID2D1Effect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Effect interface


## -description


Represents a basic image-processing construct in Direct2D.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Effect</b> interface inherits from <a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>. <b>ID2D1Effect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Effect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fca22cc2-2299-4f74-8dc9-d931b899d4fb">GetInput</a>
</td>
<td align="left" width="63%">
Gets the given input image by index. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44c719d4-29dd-4389-bdc9-63f6d533f162">GetInputCount</a>
</td>
<td align="left" width="63%">
Gets the number of inputs to the effect. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e14066f7-b195-44f1-a952-1b6c9f3832cf">GetOutput</a>
</td>
<td align="left" width="63%">
Gets the output image from the effect. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16db95e8-43e7-403c-bce1-dd2f42e81d6a">SetInput</a>
</td>
<td align="left" width="63%">
Sets the given input image by index. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdcaa997-acbe-40e3-9439-629b3853d8d4">SetInputCount</a>
</td>
<td align="left" width="63%">
Allows the application to change the number of inputs to an effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/361B0644-7437-47DA-A34C-0234EE4E92C3">SetInputEffect</a>
</td>
<td align="left" width="63%">
Sets the given input effect by index. 

</td>
</tr>
</table> 


## -remarks



An effect takes zero or more input images, and has an output image. The images that are input into and output from an effect are lazily evaluated. This definition is sufficient to allow an arbitrary graph of effects to be created from the application by feeding output images into the input image of the next effect in the chain.




## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

