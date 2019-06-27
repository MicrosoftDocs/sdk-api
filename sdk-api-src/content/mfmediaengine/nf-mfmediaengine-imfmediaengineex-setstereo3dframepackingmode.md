---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetStereo3DFramePackingMode
title: IMFMediaEngineEx::SetStereo3DFramePackingMode (mfmediaengine.h)
author: windows-sdk-content
description: For stereoscopic 3D video, sets the layout of the two views within a video frame.
old-location: mf\imfmediaengineex_setstereo3dframepackingmode.htm
tech.root: medfound
ms.assetid: E6B1EFA3-188E-495C-A38C-9CD48214BD23
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetStereo3DFramePackingMode method, IMFMediaEngineEx.SetStereo3DFramePackingMode, IMFMediaEngineEx::SetStereo3DFramePackingMode, SetStereo3DFramePackingMode, SetStereo3DFramePackingMode method [Media Foundation], SetStereo3DFramePackingMode method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setstereo3dframepackingmode, mfmediaengine/IMFMediaEngineEx::SetStereo3DFramePackingMode
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineEx.SetStereo3DFramePackingMode"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.SetStereo3DFramePackingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineEx::SetStereo3DFramePackingMode


## -description


For stereoscopic 3D video, sets the layout of the two views within a video frame.


## -parameters




### -param packMode [in]

A member of the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_s3d_packing_mode">MF_MEDIA_ENGINE_S3D_PACKING_MODE</a> enumeration that specifies the layout. The two views can be arranged side-by-side, or top-to-bottom.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
 

 

