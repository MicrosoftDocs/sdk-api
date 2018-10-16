---
UID: NN:d2d1_3.ID2D1ImageSourceFromWic
title: ID2D1ImageSourceFromWic
author: windows-sdk-content
description: Produces 2D pixel data that has been sourced from WIC.
old-location: direct2d\id2d1imagesourcefromwic.htm
tech.root: direct2d
ms.assetid: EA1F1377-A314-4375-AB86-A36CFE5AF0C8
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ID2D1ImageSourceFromWic, ID2D1ImageSourceFromWic interface [Direct2D], ID2D1ImageSourceFromWic interface [Direct2D],described, d2d1_3/ID2D1ImageSourceFromWic, direct2d.id2d1imagesourcefromwic
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
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
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1ImageSourceFromWic
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ImageSourceFromWic interface


## -description


Produces 2D pixel data that has been sourced from WIC.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1ImageSourceFromWic</b> interface inherits from <a href="https://msdn.microsoft.com/a9ee20db-98cf-bc5f-96d8-232073810cc5">ID2D1ImageSource</a>. <b>ID2D1ImageSourceFromWic</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1ImageSourceFromWic</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9addc82b-7446-1f2c-5666-f817b8b5707d">EnsureCached</a>
</td>
<td align="left" width="63%">Overloaded. Loads image data into caches of image sources if that data is not already cached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B7E2FD7F-1427-46D9-B638-6A0FF86042B4">GetSource</a>
</td>
<td align="left" width="63%">
Retrieves the underlying bitmap image source from the Windows Imaging Component (WIC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04e6e010-3642-6775-8a95-f20ff0461b09">TrimCache</a>
</td>
<td align="left" width="63%">Overloaded. Trims the populated regions of the image source cache to just the specified rectangle.

</td>
</tr>
</table> 


## -remarks



Create an an instance of ID2D1ImageSourceFromWic 
          using <a href="https://msdn.microsoft.com/af02630d-a9ca-f5b4-6f2a-31a73ef603e5">ID2D1DeviceContext2::CreateImageSourceFromWic</a>.
        



