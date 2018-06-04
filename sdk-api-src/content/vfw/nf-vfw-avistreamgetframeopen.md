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

# AVIStreamGetFrameOpen function


## -description



The <b>AVIStreamGetFrameOpen</b> function prepares to decompress video frames from the specified video stream.




## -parameters




### -param pavi

Pointer to the video stream used as the video source.


### -param lpbiWanted

Pointer to a structure that defines the desired video format. Specify <b>NULL</b> to use a default format. You can also specify AVIGETFRAMEF_BESTDISPLAYFMT to decode the frames to the best format for your display.


## -returns



Returns a <b>GetFrame</b> object that can be used with the <a href="https://msdn.microsoft.com/9677efee-4c40-4acd-8911-eedcbee67d6b">AVIStreamGetFrame</a> function. If the system cannot find a decompressor that can decompress the stream to the given format, or to any RGB format, the function returns <b>NULL</b>.

The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

