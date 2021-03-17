---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC
title: D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC (d3d11.h)
description: Describes a video processor output view.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC","D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC structure [Media Foundation]","d3d11/D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC","mf.d3d11_video_processor_output_view_desc"]
old-location: mf\d3d11_video_processor_output_view_desc.htm
tech.root: mf
ms.assetid: 8E0D44C1-220C-4E70-8A60-591AEBC16A2B
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC, D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC, mf.d3d11_video_processor_output_view_desc
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC
 - d3d11/D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC
---

# D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC structure


## -description

Describes a video processor output view.

## -struct-fields

### -field ViewDimension

The resource type of the view, specified as a member of the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_vpov_dimension">D3D11_VPOV_DIMENSION</a> enumeration.

### -field Texture2D

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_vpov">D3D11_TEX2D_VPOV</a> structure that identifies the texture resource for the output view. 

Use this member of the union when <b>ViewDimension</b> equals <b>D3D11_VPOV_DIMENSION_TEXTURE2D</b>.

### -field Texture2DArray

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_array_vpov">D3D11_TEX2D_ARRAY_VPOV</a> structure that identifies the texture array for the output view. 

Use this member of the union when <b>ViewDimension</b> equals <b>D3D11_VPOV_DIMENSION_TEXTURE2DARRAY</b>.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessoroutputview">ID3D11VideoDevice::CreateVideoProcessorOutputView</a>