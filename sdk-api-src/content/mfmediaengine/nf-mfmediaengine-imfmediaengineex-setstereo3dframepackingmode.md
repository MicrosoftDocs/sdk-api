---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetStereo3DFramePackingMode
title: IMFMediaEngineEx::SetStereo3DFramePackingMode
author: windows-sdk-content
description: For stereoscopic 3D video, sets the layout of the two views within a video frame.
old-location: mf\imfmediaengineex_setstereo3dframepackingmode.htm
old-project: medfound
ms.assetid: E6B1EFA3-188E-495C-A38C-9CD48214BD23
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetStereo3DFramePackingMode method, IMFMediaEngineEx.SetStereo3DFramePackingMode, IMFMediaEngineEx::SetStereo3DFramePackingMode, SetStereo3DFramePackingMode, SetStereo3DFramePackingMode method [Media Foundation], SetStereo3DFramePackingMode method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setstereo3dframepackingmode, mfmediaengine/IMFMediaEngineEx::SetStereo3DFramePackingMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineEx::SetStereo3DFramePackingMode


## -description


For stereoscopic 3D video, sets the layout of the two views within a video frame.


## -parameters




### -param packMode [in]

A member of the <a href="https://msdn.microsoft.com/13638568-11BE-4D1B-897E-5F8472C03677">MF_MEDIA_ENGINE_S3D_PACKING_MODE</a> enumeration that specifies the layout. The two views can be arranged side-by-side, or top-to-bottom.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

