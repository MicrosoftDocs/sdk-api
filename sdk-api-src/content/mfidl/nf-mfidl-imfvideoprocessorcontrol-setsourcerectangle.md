---
UID: NF:mfidl.IMFVideoProcessorControl.SetSourceRectangle
title: IMFVideoProcessorControl::SetSourceRectangle (mfidl.h)
description: Sets the source rectangle. (IMFVideoProcessorControl.SetSourceRectangle)
helpviewer_keywords: ["IMFVideoProcessorControl interface [Media Foundation]","SetSourceRectangle method","IMFVideoProcessorControl.SetSourceRectangle","IMFVideoProcessorControl::SetSourceRectangle","SetSourceRectangle","SetSourceRectangle method [Media Foundation]","SetSourceRectangle method [Media Foundation]","IMFVideoProcessorControl interface","mf.imfvideoprocessorcontrol_setsourcerectangle","mfidl/IMFVideoProcessorControl::SetSourceRectangle"]
old-location: mf\imfvideoprocessorcontrol_setsourcerectangle.htm
tech.root: mf
ms.assetid: 0A4E74BB-6F98-4610-9F47-5BD1E58B8589
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessorControl interface [Media Foundation],SetSourceRectangle method, IMFVideoProcessorControl.SetSourceRectangle, IMFVideoProcessorControl::SetSourceRectangle, SetSourceRectangle, SetSourceRectangle method [Media Foundation], SetSourceRectangle method [Media Foundation],IMFVideoProcessorControl interface, mf.imfvideoprocessorcontrol_setsourcerectangle, mfidl/IMFVideoProcessorControl::SetSourceRectangle
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
 - IMFVideoProcessorControl::SetSourceRectangle
 - mfidl/IMFVideoProcessorControl::SetSourceRectangle
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
 - IMFVideoProcessorControl.SetSourceRectangle
---

# IMFVideoProcessorControl::SetSourceRectangle


## -description

Sets the source rectangle. The source rectangle is the portion of the input frame that is blitted to the destination surface.

## -parameters

### -param pSrcRect

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the source rectangle.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

See <a href="/windows/desktop/medfound/video-processor-mft">Video Processor MFT</a> for info regarding source and destination rectangles in the <b>Video Processor MFT</b>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol">IMFVideoProcessorControl</a>
