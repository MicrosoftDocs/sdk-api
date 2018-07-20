---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamLumaKey
title: ID3D11VideoContext::VideoProcessorGetStreamLumaKey
author: windows-sdk-content
description: Gets the luma key for an input stream of the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetstreamlumakey.htm
old-project: medfound
ms.assetid: 1DE22456-84E9-478F-A6CA-4C9CACF7E9AF
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamLumaKey method, ID3D11VideoContext.VideoProcessorGetStreamLumaKey, ID3D11VideoContext::VideoProcessorGetStreamLumaKey, VideoProcessorGetStreamLumaKey, VideoProcessorGetStreamLumaKey method [Media Foundation], VideoProcessorGetStreamLumaKey method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamLumaKey, mf.id3d11videocontext_videoprocessorgetstreamlumakey
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorGetStreamLumaKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::VideoProcessorGetStreamLumaKey


## -description


Gets the luma key for an input stream of the video processor.




## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pEnabled [out]

Receives the value <b>TRUE</b> if luma keying is enabled, or <b>FALSE</b> otherwise.


### -param pLower [out]

Receives the lower bound for the luma key. The valid range is [0…1]. 


### -param pUpper [out]

Receives the upper bound for the luma key. The valid range is [0…1]. 


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

