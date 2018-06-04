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

# IMSVidVideoRenderer::put_SourceSize


## -description


The <b>put_SourceSize</b> method specifies the type of clipping to apply to the video rectangle, if any.


## -parameters




### -param NewSize [in]

Specifies a member of the <a href="https://msdn.microsoft.com/579c4993-6238-47c7-b61c-398568c1fb94">SourceSizeList</a> enumeration.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/312a2c1e-5332-4a2d-ada9-1dc8236f4170">IMSVidVideoRenderer::get_SourceSize</a>



<a href="https://msdn.microsoft.com/c72d8134-ff6c-46b4-b567-35638aef53cd">IMSVidVideoRenderer::put_ClippedSourceRect</a>



<a href="https://msdn.microsoft.com/141df99b-4fc7-439c-953e-1fa1c544258e">IMSVidVideoRenderer::put_OverScan</a>
 

 

