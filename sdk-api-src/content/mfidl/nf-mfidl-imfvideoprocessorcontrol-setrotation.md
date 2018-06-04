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

# IMFVideoProcessorControl::SetRotation


## -description


Specifies whether to rotate the video to the correct orientation.


## -parameters




### -param eRotation

A <a href="https://msdn.microsoft.com/B5B75A2A-6620-4E5B-8074-3A9E2FFB40F8">MF_VIDEO_PROCESSOR_ROTATION</a> value that specifies whether to rotate the image.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The original orientation of the video is specified by the <a href="https://msdn.microsoft.com/7C0911A6-6D7C-4510-891F-A6F56CE1EC2B">MF_MT_VIDEO_ROTATION</a> attribute of the input media type.

 If <i>eRotation</i> is <b>ROTATION_NONE</b>, the video processor does not correct the orientation of the output video. If the original video is rotated, and <i>eRotation</i> is <b>ROTATION_NORMAL</b>, the video processor corrects the orientation, so that the ouput video is not rotated. The video processor letterboxes the output as needed.




## -see-also




<a href="https://msdn.microsoft.com/6803B69E-CF84-45D5-804C-BD961BD5E13D">IMFVideoProcessorControl</a>
 

 

