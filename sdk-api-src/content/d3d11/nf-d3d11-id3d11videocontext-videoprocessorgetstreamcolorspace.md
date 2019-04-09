---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamColorSpace
title: ID3D11VideoContext::VideoProcessorGetStreamColorSpace (d3d11.h)
author: windows-sdk-content
description: Gets the color space for an input stream of the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetstreamcolorspace.htm
tech.root: medfound
ms.assetid: 4D66147C-D4FC-40BC-B406-B40B6EA24D94
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamColorSpace method, ID3D11VideoContext.VideoProcessorGetStreamColorSpace, ID3D11VideoContext::VideoProcessorGetStreamColorSpace, VideoProcessorGetStreamColorSpace, VideoProcessorGetStreamColorSpace method [Media Foundation], VideoProcessorGetStreamColorSpace method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamColorSpace, mf.id3d11videocontext_videoprocessorgetstreamcolorspace
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
 - ID3D11VideoContext.VideoProcessorGetStreamColorSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetStreamColorSpace


## -description


Gets the color space for an input stream of the video processor.




## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pColorSpace [out]

Receives a <a href="https://msdn.microsoft.com/D5F36CFC-ED36-47F3-A07A-9B163F904D74">D3D11_VIDEO_PROCESSOR_COLOR_SPACE</a> value that specifies the color space.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

