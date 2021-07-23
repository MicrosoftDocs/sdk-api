---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetStereo3DRenderMode
title: IMFMediaEngineEx::GetStereo3DRenderMode (mfmediaengine.h)
description: For stereoscopic 3D video, queries how the Media Engine renders the 3D video content.
helpviewer_keywords: ["GetStereo3DRenderMode","GetStereo3DRenderMode method [Media Foundation]","GetStereo3DRenderMode method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetStereo3DRenderMode method","IMFMediaEngineEx.GetStereo3DRenderMode","IMFMediaEngineEx::GetStereo3DRenderMode","mf.imfmediaengineex_getstereo3drendermode","mfmediaengine/IMFMediaEngineEx::GetStereo3DRenderMode"]
old-location: mf\imfmediaengineex_getstereo3drendermode.htm
tech.root: mf
ms.assetid: 204C9B35-860F-46FD-AF3F-7BC7E1EE12EF
ms.date: 12/05/2018
ms.keywords: GetStereo3DRenderMode, GetStereo3DRenderMode method [Media Foundation], GetStereo3DRenderMode method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetStereo3DRenderMode method, IMFMediaEngineEx.GetStereo3DRenderMode, IMFMediaEngineEx::GetStereo3DRenderMode, mf.imfmediaengineex_getstereo3drendermode, mfmediaengine/IMFMediaEngineEx::GetStereo3DRenderMode
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
 - IMFMediaEngineEx::GetStereo3DRenderMode
 - mfmediaengine/IMFMediaEngineEx::GetStereo3DRenderMode
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
 - IMFMediaEngineEx.GetStereo3DRenderMode
---

# IMFMediaEngineEx::GetStereo3DRenderMode


## -description

For stereoscopic 3D video, queries how the Media Engine renders the 3D video content.

## -parameters

### -param outputType [out]

Receives a member of the <a href="/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype">MF3DVideoOutputType</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>