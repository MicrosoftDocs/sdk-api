---
UID: NF:mfidl.IMFVideoProcessorControl.SetRotation
title: IMFVideoProcessorControl::SetRotation (mfidl.h)
description: Specifies whether to rotate the video to the correct orientation.
helpviewer_keywords: ["IMFVideoProcessorControl interface [Media Foundation]","SetRotation method","IMFVideoProcessorControl.SetRotation","IMFVideoProcessorControl::SetRotation","SetRotation","SetRotation method [Media Foundation]","SetRotation method [Media Foundation]","IMFVideoProcessorControl interface","mf.imfvideoprocessorcontrol_setrotation","mfidl/IMFVideoProcessorControl::SetRotation"]
old-location: mf\imfvideoprocessorcontrol_setrotation.htm
tech.root: mf
ms.assetid: 452FE057-EC1A-430E-A5C8-C9B84A4B1B17
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessorControl interface [Media Foundation],SetRotation method, IMFVideoProcessorControl.SetRotation, IMFVideoProcessorControl::SetRotation, SetRotation, SetRotation method [Media Foundation], SetRotation method [Media Foundation],IMFVideoProcessorControl interface, mf.imfvideoprocessorcontrol_setrotation, mfidl/IMFVideoProcessorControl::SetRotation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoProcessorControl::SetRotation
 - mfidl/IMFVideoProcessorControl::SetRotation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl.SetRotation
---

# IMFVideoProcessorControl::SetRotation


## -description

Specifies whether to rotate the video to the correct orientation.

## -parameters

### -param eRotation

A <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_video_processor_rotation">MF_VIDEO_PROCESSOR_ROTATION</a> value that specifies whether to rotate the image.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The original orientation of the video is specified by the <a href="/windows/desktop/medfound/mf-mt-video-rotation">MF_MT_VIDEO_ROTATION</a> attribute of the input media type.

 If <i>eRotation</i> is <b>ROTATION_NONE</b>, the video processor does not correct the orientation of the output video. If the original video is rotated, and <i>eRotation</i> is <b>ROTATION_NORMAL</b>, the video processor corrects the orientation, so that the output video is not rotated. The video processor letterboxes the output as needed.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol">IMFVideoProcessorControl</a>