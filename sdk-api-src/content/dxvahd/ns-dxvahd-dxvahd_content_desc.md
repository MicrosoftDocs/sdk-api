---
UID: NS:dxvahd._DXVAHD_CONTENT_DESC
title: DXVAHD_CONTENT_DESC (dxvahd.h)
description: Describes a video stream for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
helpviewer_keywords: ["DXVAHD_CONTENT_DESC","DXVAHD_CONTENT_DESC structure [Media Foundation]","dxvahd/DXVAHD_CONTENT_DESC","mf.dxvahd_content_desc"]
old-location: mf\dxvahd_content_desc.htm
tech.root: mf
ms.assetid: 9319a98d-8f43-4f29-8787-18dec53dff88
ms.date: 12/05/2018
ms.keywords: DXVAHD_CONTENT_DESC, DXVAHD_CONTENT_DESC structure [Media Foundation], dxvahd/DXVAHD_CONTENT_DESC, mf.dxvahd_content_desc
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_CONTENT_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_CONTENT_DESC
 - dxvahd/_DXVAHD_CONTENT_DESC
 - DXVAHD_CONTENT_DESC
 - dxvahd/DXVAHD_CONTENT_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_CONTENT_DESC
---

# DXVAHD_CONTENT_DESC structure


## -description

Describes a video stream for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

The display driver can use the information in this structure to optimize the capabilities of the video processor. For example, some capabilities might not be exposed for high-definition (HD) content, for performance reasons.

## -struct-fields

### -field InputFrameFormat

A member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_frame_format">DXVAHD_FRAME_FORMAT</a> enumeration that describes how the video stream is interlaced.

### -field InputFrameRate

The frame rate of the input video stream, specified as a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_rational">DXVAHD_RATIONAL</a> structure.

### -field InputWidth

The width of the input frames, in pixels.

### -field InputHeight

The height of the input frames, in pixels.

### -field OutputFrameRate

The frame rate of the output video stream, specified as a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_rational">DXVAHD_RATIONAL</a> structure.

### -field OutputWidth

The width of the output frames, in pixels.

### -field OutputHeight

The height of the output frames, in pixels.

## -remarks

Frame rates are expressed as ratios. For example, 30 frames per second (fps) is expressed as 30:1, and 29.97 fps is expressed as 30000/1001. For interlaced content, a frame consists of two fields, so that the frame rate is half the field rate.
      

 If the application will composite two or more input streams, use the largest stream for the values of <b>InputWidth</b> and <b>InputHeight</b>.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>