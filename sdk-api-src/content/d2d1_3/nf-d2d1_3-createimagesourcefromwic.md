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
 

 

