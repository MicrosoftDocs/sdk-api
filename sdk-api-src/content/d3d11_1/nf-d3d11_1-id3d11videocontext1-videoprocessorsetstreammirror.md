---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorSetStreamMirror
title: ID3D11VideoContext1::VideoProcessorSetStreamMirror
author: windows-driver-content
description: Specifies whether the video processor input stream should be flipped vertically or horizontally.
old-location: mf\id3d11videocontext1_videoprocessorsetstreammirror.htm
old-project: medfound
ms.assetid: C8CCCC2B-B05A-4AF4-9274-1E205B9807DB
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorSetStreamMirror method, ID3D11VideoContext1.VideoProcessorSetStreamMirror, ID3D11VideoContext1::VideoProcessorSetStreamMirror, VideoProcessorSetStreamMirror, VideoProcessorSetStreamMirror method [Media Foundation], VideoProcessorSetStreamMirror method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorSetStreamMirror, mf.id3d11videocontext1_videoprocessorsetstreammirror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11_1.h
api_name:
-	ID3D11VideoContext1.VideoProcessorSetStreamMirror
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext1::VideoProcessorSetStreamMirror


## -description


Specifies whether the video processor input stream should be flipped vertically or horizontally.


## -parameters




### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface.


### -param StreamIndex [in]

Type: <b>UINT</b>

An index identifying the input stream.


### -param Enable [in]

Type: <b>BOOL</b>

True if mirroring should be enabled; otherwise, false.


### -param FlipHorizontal [in]

Type: <b>BOOL</b>

True if the stream should be flipped horizontally; otherwise, false.


### -param FlipVertical [in]

Type: <b>BOOL</b>

True if the stream should be flipped vertically; otherwise, false.


## -returns



This method does not return a value.




## -remarks



When used in combination, transformations on the processor input stream should be applied in the following order:

<ul>
<li>Rotation</li>
<li>Mirroring</li>
<li>Source clipping</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

