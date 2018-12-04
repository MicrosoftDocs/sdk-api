---
UID: NF:mfidl.IMFVideoProcessorControl.SetRotation
title: IMFVideoProcessorControl::SetRotation
author: windows-sdk-content
description: Specifies whether to rotate the video to the correct orientation.
old-location: mf\imfvideoprocessorcontrol_setrotation.htm
tech.root: medfound
ms.assetid: 452FE057-EC1A-430E-A5C8-C9B84A4B1B17
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IMFVideoProcessorControl interface [Media Foundation],SetRotation method, IMFVideoProcessorControl.SetRotation, IMFVideoProcessorControl::SetRotation, SetRotation, SetRotation method [Media Foundation], SetRotation method [Media Foundation],IMFVideoProcessorControl interface, mf.imfvideoprocessorcontrol_setrotation, mfidl/IMFVideoProcessorControl::SetRotation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl.SetRotation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

