---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetStereo3DFramePackingMode
title: IMFMediaEngineEx::GetStereo3DFramePackingMode method
author: windows-driver-content
description: For stereoscopic 3D video, gets the layout of the two views within a video frame.
old-location: mf\imfmediaengineex_getstereo3dframepackingmode.htm
old-project: medfound
ms.assetid: 003204DB-DDAD-4F72-BA25-015B033BAC92
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetStereo3DFramePackingMode method [Media Foundation], GetStereo3DFramePackingMode method [Media Foundation], IMFMediaEngineEx interface, GetStereo3DFramePackingMode,IMFMediaEngineEx.GetStereo3DFramePackingMode, IMFMediaEngineEx, IMFMediaEngineEx interface [Media Foundation], GetStereo3DFramePackingMode method, IMFMediaEngineEx::GetStereo3DFramePackingMode, mf.imfmediaengineex_getstereo3dframepackingmode, mfmediaengine/IMFMediaEngineEx::GetStereo3DFramePackingMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineEx.GetStereo3DFramePackingMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineEx::GetStereo3DFramePackingMode method


## -description


For stereoscopic 3D video, gets the layout of the two views within a video frame.


## -parameters




### -param packMode [out]

Receives a member of the <a href="https://msdn.microsoft.com/13638568-11BE-4D1B-897E-5F8472C03677">MF_MEDIA_ENGINE_S3D_PACKING_MODE</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

