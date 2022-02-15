---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetStereo3DRenderMode
title: IMFMediaEngineEx::SetStereo3DRenderMode (mfmediaengine.h)
description: For stereoscopic 3D video, specifies how the Media Engine renders the 3D video content.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","SetStereo3DRenderMode method","IMFMediaEngineEx.SetStereo3DRenderMode","IMFMediaEngineEx::SetStereo3DRenderMode","SetStereo3DRenderMode","SetStereo3DRenderMode method [Media Foundation]","SetStereo3DRenderMode method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_setstereo3drendermode","mfmediaengine/IMFMediaEngineEx::SetStereo3DRenderMode"]
old-location: mf\imfmediaengineex_setstereo3drendermode.htm
tech.root: mf
ms.assetid: 89B6B2AC-A721-4C56-BF0A-A19350FE4823
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetStereo3DRenderMode method, IMFMediaEngineEx.SetStereo3DRenderMode, IMFMediaEngineEx::SetStereo3DRenderMode, SetStereo3DRenderMode, SetStereo3DRenderMode method [Media Foundation], SetStereo3DRenderMode method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setstereo3drendermode, mfmediaengine/IMFMediaEngineEx::SetStereo3DRenderMode
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
 - IMFMediaEngineEx::SetStereo3DRenderMode
 - mfmediaengine/IMFMediaEngineEx::SetStereo3DRenderMode
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
 - IMFMediaEngineEx.SetStereo3DRenderMode
---

# IMFMediaEngineEx::SetStereo3DRenderMode


## -description

For stereoscopic 3D video, specifies how the Media Engine renders the 3D video content.

## -parameters

### -param outputType [in]

A member of the <a href="/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype">MF3DVideoOutputType</a> enumeration that specifies the 3D video rendering mode.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>