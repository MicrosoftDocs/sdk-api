---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamAlpha
title: ID3D11VideoContext::VideoProcessorGetStreamAlpha
author: windows-sdk-content
description: Gets the planar alpha for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetstreamalpha.htm
tech.root: medfound
ms.assetid: E2DB0672-54D9-4DDB-B6EA-9935237C33FB
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamAlpha method, ID3D11VideoContext.VideoProcessorGetStreamAlpha, ID3D11VideoContext::VideoProcessorGetStreamAlpha, VideoProcessorGetStreamAlpha, VideoProcessorGetStreamAlpha method [Media Foundation], VideoProcessorGetStreamAlpha method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamAlpha, mf.id3d11videocontext_videoprocessorgetstreamalpha
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorGetStreamAlpha
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetStreamAlpha


## -description


Gets the planar alpha for an input stream on the video processor.




## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pEnabled [out]

Receives the value <b>TRUE</b> if planar alpha is enabled, or <b>FALSE</b> otherwise.


### -param pAlpha [out]

Receives the planar alpha value. The value can range from 0.0 (transparent) to 1.0 (opaque).


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

