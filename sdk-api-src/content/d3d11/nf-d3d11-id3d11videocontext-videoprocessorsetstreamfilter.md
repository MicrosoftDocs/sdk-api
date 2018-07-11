---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamFilter
title: ID3D11VideoContext::VideoProcessorSetStreamFilter
author: windows-sdk-content
description: Enables or disables an image filter for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetstreamfilter.htm
old-project: medfound
ms.assetid: 49258E8F-50BC-4F51-A492-78B44A73CC13
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamFilter method, ID3D11VideoContext.VideoProcessorSetStreamFilter, ID3D11VideoContext::VideoProcessorSetStreamFilter, VideoProcessorSetStreamFilter, VideoProcessorSetStreamFilter method [Media Foundation], VideoProcessorSetStreamFilter method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamFilter, mf.id3d11videocontext_videoprocessorsetstreamfilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
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
 - ID3D11VideoContext.VideoProcessorSetStreamFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::VideoProcessorSetStreamFilter


## -description


Enables or disables an image filter for an input stream on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Filter [in]

The filter, specified as a <a href="https://msdn.microsoft.com/87CF9A1A-E196-4B5A-BAAE-DD948A5468C2">D3D11_VIDEO_PROCESSOR_FILTER</a> value.

To query which filters the driver supports, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>.


### -param Enable [in]

Specifies whether to enable the filter.


### -param Level [in]

The filter level. If <i>Enable</i> is <b>FALSE</b>, this parameter is ignored. 

To find the valid range of levels for a specified filter, call <a href="https://msdn.microsoft.com/F43A01D7-A0FE-4509-B3B2-094B09A7F04A">ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange</a>.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

