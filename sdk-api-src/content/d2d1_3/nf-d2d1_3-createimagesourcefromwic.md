---
UID: NF:d2d1_3.CreateImageSourceFromWic
title: CreateImageSourceFromWic function
author: windows-sdk-content
description: Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source. The image is loaded and stored while using a minimal amount of memory.
old-location: direct2d\id2d1devicecontext2_createimagesourcefromwic_overload.htm
old-project: direct2d
ms.assetid: af02630d-a9ca-f5b4-6f2a-31a73ef603e5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateImageSourceFromWic, CreateImageSourceFromWic methods [Direct2D], ID2D1DeviceContext2::CreateImageSourceFromWic, d2d1_3/CreateImageSourceFromWic, direct2d.id2d1devicecontext2_createimagesourcefromwic_overload
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_3.h
api_name:
 - ID2D1DeviceContext2::CreateImageSourceFromWic
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CreateImageSourceFromWic function


## -description


<span>Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.  The image is loaded and stored while using a minimal amount of memory.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be72278a-f901-8f6a-53de-b6fd57e0fc3a">CreateImageSourceFromWic (IWICBitmapSource*, D2D1_IMAGE_SOURCE_LOADING_OPTIONS, ID2D1ImageSourceFromWic**)</a>
</td>
<td align="left" width="63%">
Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options with default alpha mode.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76f92adf-6bb5-d80f-6deb-7edc92170f54">CreateImageSourceFromWic (IWICBitmapSource*, D2D1_IMAGE_SOURCE_LOADING_OPTIONS, D2D1_ALPHA_MODE, ID2D1ImageSourceFromWic**)</a>
</td>
<td align="left" width="63%">
Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options, and alpha mode.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78e39978-099f-1096-ed7a-5b2dc68bb9c3">CreateImageSourceFromWic (IWICBitmapSource*, ID2D1ImageSourceFromWic**)</a>
</td>
<td align="left" width="63%">
Version of the method that allows you to specify the WIC bitmap source and the output image source object with default loading opitons and alpha mode.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a>
 

 

