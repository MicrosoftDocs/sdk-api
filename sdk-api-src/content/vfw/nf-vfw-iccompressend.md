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

# ICCompressEnd macro


## -description



The <b>ICCompressEnd</b> macro notifies a video compression driver to end compression and free resources allocated for compression. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/5d4b5962-c4f0-44eb-a3a9-36026f167a5a">ICM_COMPRESS_END</a> message.




## -parameters




### -param hic

Handle of the compressor. 


## -remarks



VCM saves the settings of the most recent <b>ICCompressBegin</b> macro. <b>ICCompressBegin</b> and <b>ICCompressEnd</b> do not nest. If your driver receives the <b>ICM_COMPRESS_BEGIN</b> message before compression is stopped with the <b>ICM_COMPRESS_END</b> message, it should restart compression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

