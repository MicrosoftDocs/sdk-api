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

# SourceSizeList enumeration


## -description



This topic applies to Windows XP or later.
        



The <b>SourceSizeList</b> enumeration is used to indicate how the VMR will clip the source video rectangle.


## -enum-fields




### -field sslFullSize

Do not clip the source video rectangle.


### -field sslClipByOverScan

Clip the source video rectangle by the value specified in the last call to <a href="https://msdn.microsoft.com/141df99b-4fc7-439c-953e-1fa1c544258e">IMSVidVideoRenderer::put_OverScan</a>.


### -field sslClipByClipRect

Clip the source video rectangle by the value specified in the last call to <a href="https://msdn.microsoft.com/c72d8134-ff6c-46b4-b567-35638aef53cd">IMSVidVideoRenderer::put_ClippedSourceRect</a>



## -see-also




<a href="https://msdn.microsoft.com/312a2c1e-5332-4a2d-ada9-1dc8236f4170">IMSVidVideoRenderer::get_SourceSize</a>



<a href="https://msdn.microsoft.com/c792f064-a137-4872-8c79-6e924b6023f0">IMSVidVideoRenderer::put_SourceSize</a>



<a href="https://msdn.microsoft.com/3c21f2c6-8eff-4fe5-a383-057f3394d9ee">Video Control Enumerations</a>
 

 

