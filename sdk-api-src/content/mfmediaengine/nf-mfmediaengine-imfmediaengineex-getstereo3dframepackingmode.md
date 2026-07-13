---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetStereo3DFramePackingMode
title: IMFMediaEngineEx::GetStereo3DFramePackingMode (mfmediaengine.h)
description: For stereoscopic 3D video, gets the layout of the two views within a video frame.
helpviewer_keywords: ["GetStereo3DFramePackingMode","GetStereo3DFramePackingMode method [Media Foundation]","GetStereo3DFramePackingMode method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetStereo3DFramePackingMode method","IMFMediaEngineEx.GetStereo3DFramePackingMode","IMFMediaEngineEx::GetStereo3DFramePackingMode","mf.imfmediaengineex_getstereo3dframepackingmode","mfmediaengine/IMFMediaEngineEx::GetStereo3DFramePackingMode"]
old-location: mf\imfmediaengineex_getstereo3dframepackingmode.htm
tech.root: mf
ms.assetid: 003204DB-DDAD-4F72-BA25-015B033BAC92
ms.date: 12/05/2018
ms.keywords: GetStereo3DFramePackingMode, GetStereo3DFramePackingMode method [Media Foundation], GetStereo3DFramePackingMode method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetStereo3DFramePackingMode method, IMFMediaEngineEx.GetStereo3DFramePackingMode, IMFMediaEngineEx::GetStereo3DFramePackingMode, mf.imfmediaengineex_getstereo3dframepackingmode, mfmediaengine/IMFMediaEngineEx::GetStereo3DFramePackingMode
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaEngineEx::GetStereo3DFramePackingMode
 - mfmediaengine/IMFMediaEngineEx::GetStereo3DFramePackingMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.GetStereo3DFramePackingMode
---

# IMFMediaEngineEx::GetStereo3DFramePackingMode


## -description

For stereoscopic 3D video, gets the layout of the two views within a video frame.

## -parameters

### -param packMode [out]

Receives a member of the <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_s3d_packing_mode">MF_MEDIA_ENGINE_S3D_PACKING_MODE</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>