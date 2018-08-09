---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamPixelAspectRatio
title: ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio
author: windows-sdk-content
description: Gets the pixel aspect ratio for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetstreampixelaspectratio.htm
old-project: medfound
ms.assetid: 45B0CF31-6552-4C75-B32F-755398D1A054
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamPixelAspectRatio method, ID3D11VideoContext.VideoProcessorGetStreamPixelAspectRatio, ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio, VideoProcessorGetStreamPixelAspectRatio, VideoProcessorGetStreamPixelAspectRatio method [Media Foundation], VideoProcessorGetStreamPixelAspectRatio method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio, mf.id3d11videocontext_videoprocessorgetstreampixelaspectratio
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
 - ID3D11VideoContext.VideoProcessorGetStreamPixelAspectRatio
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio


## -description


Gets the pixel aspect ratio for an input stream on the video processor.




## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pEnabled [out]

Receives the value <b>TRUE</b> if the pixel aspect ratio is specified. Otherwise, receives the value <b>FALSE</b>.


### -param pSourceAspectRatio [out]

A pointer to a <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure. If *<i>pEnabled</i> is <b>TRUE</b>, this parameter receives the pixel aspect ratio of the source rectangle.


### -param pDestinationAspectRatio [out]

A pointer to a <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure. If *<i>pEnabled</i> is <b>TRUE</b>, this parameter receives the pixel aspect ratio of the destination rectangle.


## -returns



This method does not return a value.




## -remarks



When the method returns, if <i>*pEnabled</i> is <b>TRUE</b>, the <i>pSourceAspectRatio</i> and <i>pDestinationAspectRatio</i> parameters contain the pixel aspect ratios. Otherwise, the default pixel aspect ratio is 1:1 (square pixels).




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

