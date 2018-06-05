---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamAutoProcessingMode
title: ID3D11VideoContext::VideoProcessorGetStreamAutoProcessingMode
author: windows-sdk-content
description: Queries whether automatic processing features of the video processor are enabled.
old-location: mf\id3d11videocontext_videoprocessorgetstreamautoprocessingmode.htm
old-project: medfound
ms.assetid: FD7B20C2-5418-4CA5-A64E-FA84D4070A10
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamAutoProcessingMode method, ID3D11VideoContext.VideoProcessorGetStreamAutoProcessingMode, ID3D11VideoContext::VideoProcessorGetStreamAutoProcessingMode, VideoProcessorGetStreamAutoProcessingMode, VideoProcessorGetStreamAutoProcessingMode method [Media Foundation], VideoProcessorGetStreamAutoProcessingMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamAutoProcessingMode, mf.id3d11videocontext_videoprocessorgetstreamautoprocessingmode
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.h
api_name:
-	ID3D11VideoContext.VideoProcessorGetStreamAutoProcessingMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::VideoProcessorGetStreamAutoProcessingMode


## -description


Queries whether automatic processing features of the video processor are enabled.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pEnabled [out]

Receives the value <b>TRUE</b> if automatic processing features are enabled, or <b>FALSE</b> otherwise.


## -returns



This method does not return a value.




## -remarks



Automatic processing  refers to additional image processing that drivers might have performed on the image data prior to the application receiving the data.   




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

