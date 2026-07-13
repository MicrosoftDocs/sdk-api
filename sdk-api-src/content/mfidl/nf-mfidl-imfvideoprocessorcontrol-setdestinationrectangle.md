---
UID: NF:mfidl.IMFVideoProcessorControl.SetDestinationRectangle
title: IMFVideoProcessorControl::SetDestinationRectangle (mfidl.h)
description: Sets the destination rectangle.
helpviewer_keywords: ["IMFVideoProcessorControl interface [Media Foundation]","SetDestinationRectangle method","IMFVideoProcessorControl.SetDestinationRectangle","IMFVideoProcessorControl::SetDestinationRectangle","SetDestinationRectangle","SetDestinationRectangle method [Media Foundation]","SetDestinationRectangle method [Media Foundation]","IMFVideoProcessorControl interface","mf.imfvideoprocessorcontrol_setdestinationrectangle","mfidl/IMFVideoProcessorControl::SetDestinationRectangle"]
old-location: mf\imfvideoprocessorcontrol_setdestinationrectangle.htm
tech.root: mf
ms.assetid: 8AD1BDF4-2508-4A99-85A1-9DBC969D511B
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessorControl interface [Media Foundation],SetDestinationRectangle method, IMFVideoProcessorControl.SetDestinationRectangle, IMFVideoProcessorControl::SetDestinationRectangle, SetDestinationRectangle, SetDestinationRectangle method [Media Foundation], SetDestinationRectangle method [Media Foundation],IMFVideoProcessorControl interface, mf.imfvideoprocessorcontrol_setdestinationrectangle, mfidl/IMFVideoProcessorControl::SetDestinationRectangle
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
 - IMFVideoProcessorControl::SetDestinationRectangle
 - mfidl/IMFVideoProcessorControl::SetDestinationRectangle
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
 - IMFVideoProcessorControl.SetDestinationRectangle
---

# IMFVideoProcessorControl::SetDestinationRectangle


## -description

Sets the destination rectangle. The destination rectangle is the portion of the output surface where the source rectangle is blitted.

## -parameters

### -param pDstRect

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the destination rectangle.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

See <a href="/windows/desktop/medfound/video-processor-mft">Video Processor MFT</a> for info regarding source and destination rectangles in the <b>Video Processor MFT</b>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol">IMFVideoProcessorControl</a>