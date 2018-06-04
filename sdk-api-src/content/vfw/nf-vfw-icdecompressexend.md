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

# ICDecompressExEnd macro


## -description



The <b>ICDecompressExEnd</b> macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/7ed63a4e-bb17-43a3-b593-25c4a51be942">ICM_DECOMPRESSEX_END</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


## -remarks



The driver frees any resources allocated for the <a href="https://msdn.microsoft.com/35298274-91b5-4df0-b4b0-4a71d6a49990">ICM_DECOMPRESSEX_BEGIN</a> message.


<a href="https://msdn.microsoft.com/35277938-6fae-4207-8b91-439af2b481e8">
          ICM_DECOMPRESSEX_BEGIN</a> and <a href="https://msdn.microsoft.com/7ed63a4e-bb17-43a3-b593-25c4a51be942">ICM_DECOMPRESSEX_END</a> do not nest. If your driver receives <a href="https://msdn.microsoft.com/35298274-91b5-4df0-b4b0-4a71d6a49990">ICM_DECOMPRESSEX_BEGIN</a> before decompression is stopped with <b>ICM_DECOMPRESSEX_END</b>, it should restart decompression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

