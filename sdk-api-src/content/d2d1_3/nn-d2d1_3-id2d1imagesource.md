---
UID: NN:d2d1_3.ID2D1ImageSource
title: ID2D1ImageSource
author: windows-sdk-content
description: Represents a producer of pixels that can fill an arbitrary 2D plane.
old-location: direct2d\id2d1imagesource.htm
tech.root: Direct2D
ms.assetid: a9ee20db-98cf-bc5f-96d8-232073810cc5
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID2D1ImageSource, ID2D1ImageSource interface [Direct2D], ID2D1ImageSource interface [Direct2D],described, d2d1_3/ID2D1ImageSource, direct2d.id2d1imagesource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ID2D1ImageSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ImageSource interface


## -description


Represents a producer of pixels that can fill an arbitrary 2D plane.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1ImageSource</b> interface inherits from <a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>. <b>ID2D1ImageSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1ImageSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35728A9D-1D86-41EB-A760-B6B56D2576F3">OfferResources</a>
</td>
<td align="left" width="63%">
Allows the operating system to free the video memory of resources by discarding their content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9639353D-EA3B-4ABD-A4DE-405B18218801">TryReclaimResources</a>
</td>
<td align="left" width="63%">
Restores access to resources that were previously offered by calling <a href="https://msdn.microsoft.com/35728A9D-1D86-41EB-A760-B6B56D2576F3">OfferResources</a>.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/af02630d-a9ca-f5b4-6f2a-31a73ef603e5">I2D1DeviceContext2::CreateImageSourceFromWic</a>



<a href="https://msdn.microsoft.com/5ea6ba4c-9bd6-a909-82d5-c4690dc9a24e">ID2D1DeviceContext2::CreateImageSourceFromDxgi</a>



<a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>



<a href="https://msdn.microsoft.com/EA1F1377-A314-4375-AB86-A36CFE5AF0C8">ID2D1ImageSourceFromWic</a>
 

 

