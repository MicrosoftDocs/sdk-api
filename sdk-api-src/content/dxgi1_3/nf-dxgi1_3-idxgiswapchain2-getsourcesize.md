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

# IDXGISwapChain2::GetSourceSize


## -description


Gets the source region used for the swap chain.

Use <b>GetSourceSize</b> to get the portion of the swap chain from which the operating system presents. The source rectangle is always defined by the region [0, 0, Width, Height]. Use <a href="https://msdn.microsoft.com/BD424F5A-9735-4E90-9FAD-A0B827D7AD80">SetSourceSize</a> to set this portion of the swap chain. 


## -parameters




### -param pWidth [out]

 The current width of the source region of the swap chain. This value can range from 1 to the overall width of the swap chain.


### -param pHeight [out]

The current height of the source region of the swap chain. This value can range from 1 to the overall height of the swap chain.


## -returns



 This method can return error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/1E14EAF6-5EEA-4B4A-8F5F-0BC779093654">IDXGISwapChain2</a>



<a href="https://msdn.microsoft.com/BD424F5A-9735-4E90-9FAD-A0B827D7AD80">SetSourceSize</a>
 

 

