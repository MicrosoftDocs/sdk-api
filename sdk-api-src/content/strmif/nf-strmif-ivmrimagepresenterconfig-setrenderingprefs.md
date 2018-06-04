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

# IVMRImagePresenterConfig::SetRenderingPrefs


## -description



The <code>SetRenderingPrefs</code> method sets the rendering preferences on the VMR-7 filter's allocator-presenter.



The VMR-7 filter's <a href="https://msdn.microsoft.com/1374d071-f396-4fcb-8ca2-ac3986960207">IVMRFilterConfig::SetRenderingPrefs</a> method calls through to this method.


## -parameters




### -param dwRenderFlags [in]

A bitwise OR combination of <a href="https://msdn.microsoft.com/cfe1d4a7-b1ec-4d8e-b6d5-3fe5a530c352">VMRRenderPrefs</a> flags that will be used to configure the allocator-presenter.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/cbf0fac4-c976-4c1a-ab3a-75ae0d565544">IVMRImagePresenterConfig Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

