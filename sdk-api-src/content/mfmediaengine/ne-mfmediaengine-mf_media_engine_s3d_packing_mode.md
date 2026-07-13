---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_S3D_PACKING_MODE
title: MF_MEDIA_ENGINE_S3D_PACKING_MODE (mfmediaengine.h)
description: Specifies the layout for a packed 3D video frame.
helpviewer_keywords: ["MF_MEDIA_ENGINE_S3D_PACKING_MODE","MF_MEDIA_ENGINE_S3D_PACKING_MODE enumeration [Media Foundation]","MF_MEDIA_ENGINE_S3D_PACKING_MODE_NONE","MF_MEDIA_ENGINE_S3D_PACKING_MODE_SIDE_BY_SIDE","MF_MEDIA_ENGINE_S3D_PACKING_MODE_TOP_BOTTOM","mf.mf_media_engine_s3d_packing_mode","mfmediaengine/MF_MEDIA_ENGINE_S3D_PACKING_MODE","mfmediaengine/MF_MEDIA_ENGINE_S3D_PACKING_MODE_NONE","mfmediaengine/MF_MEDIA_ENGINE_S3D_PACKING_MODE_SIDE_BY_SIDE","mfmediaengine/MF_MEDIA_ENGINE_S3D_PACKING_MODE_TOP_BOTTOM"]
old-location: mf\mf_media_engine_s3d_packing_mode.htm
tech.root: mf
ms.assetid: 13638568-11BE-4D1B-897E-5F8472C03677
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_S3D_PACKING_MODE, MF_MEDIA_ENGINE_S3D_PACKING_MODE enumeration [Media Foundation], MF_MEDIA_ENGINE_S3D_PACKING_MODE_NONE, MF_MEDIA_ENGINE_S3D_PACKING_MODE_SIDE_BY_SIDE, MF_MEDIA_ENGINE_S3D_PACKING_MODE_TOP_BOTTOM, mf.mf_media_engine_s3d_packing_mode, mfmediaengine/MF_MEDIA_ENGINE_S3D_PACKING_MODE, mfmediaengine/MF_MEDIA_ENGINE_S3D_PACKING_MODE_NONE, mfmediaengine/MF_MEDIA_ENGINE_S3D_PACKING_MODE_SIDE_BY_SIDE, mfmediaengine/MF_MEDIA_ENGINE_S3D_PACKING_MODE_TOP_BOTTOM
req.header: mfmediaengine.h
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
req.typenames: MF_MEDIA_ENGINE_S3D_PACKING_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_MEDIA_ENGINE_S3D_PACKING_MODE
 - mfmediaengine/MF_MEDIA_ENGINE_S3D_PACKING_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_S3D_PACKING_MODE
---

# MF_MEDIA_ENGINE_S3D_PACKING_MODE enumeration


## -description

Specifies the layout for a packed 3D video frame.

## -enum-fields

### -field MF_MEDIA_ENGINE_S3D_PACKING_MODE_NONE:0

None.

### -field MF_MEDIA_ENGINE_S3D_PACKING_MODE_SIDE_BY_SIDE:1

The views are packed side-by-side in a single frame.

### -field MF_MEDIA_ENGINE_S3D_PACKING_MODE_TOP_BOTTOM:2

The views are packed top-to-bottom in a single frame.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getstereo3dframepackingmode">IMFMediaEngineEx::GetStereo3DFramePackingMode</a>



<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setstereo3dframepackingmode">IMFMediaEngineEx::SetStereo3DFramePackingMode</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
