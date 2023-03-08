---
UID: NC:dxvahd.PDXVAHDSW_VideoProcessBltHD
title: PDXVAHDSW_VideoProcessBltHD (dxvahd.h)
description: Performs a video processing blit.
helpviewer_keywords: ["PDXVAHDSW_VideoProcessBltHD","PDXVAHDSW_VideoProcessBltHD callback","PDXVAHDSW_VideoProcessBltHD callback function [Media Foundation]","dxvahd/PDXVAHDSW_VideoProcessBltHD","mf.pdxvahdsw_videoprocessblthd"]
old-location: mf\pdxvahdsw_videoprocessblthd.htm
tech.root: mf
ms.assetid: 94e6b59f-dd00-4d32-b1ca-a592a67cd0ec
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_VideoProcessBltHD, PDXVAHDSW_VideoProcessBltHD callback, PDXVAHDSW_VideoProcessBltHD callback function [Media Foundation], dxvahd/PDXVAHDSW_VideoProcessBltHD, mf.pdxvahdsw_videoprocessblthd
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDXVAHDSW_VideoProcessBltHD
 - dxvahd/PDXVAHDSW_VideoProcessBltHD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxvahd.h
api_name:
 - PDXVAHDSW_VideoProcessBltHD
---

# PDXVAHDSW_VideoProcessBltHD callback function


## -description

Performs a video processing blit.

## -parameters

### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.

### -param pOutputSurface [in]

A pointer to the <b>IDirect3DSurface9</b> interface of a Direct3D surface that receives the blit.

### -param OutputFrame [in]

The frame number of the output video frame, indexed from zero.

### -param StreamCount [in]

The number of input streams to process.

### -param pStreams [in]

A pointer to an array of <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_data">DXVAHD_STREAM_DATA</a> structures that contain information about the input streams. The number of elements in the array is given in the <i>StreamCount</i> parameter.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-videoprocessblthd">IDXVAHD_VideoProcessor::VideoProcessBltHD</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
