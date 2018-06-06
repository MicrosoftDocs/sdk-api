---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_STREAM
title: D3D11_VIDEO_PROCESSOR_STREAM
author: windows-sdk-content
description: Contains stream-level data for the ID3D11VideoContext::VideoProcessorBlt method.
old-location: mf\d3d11_video_processor_stream.htm
old-project: medfound
ms.assetid: B861D00B-2FF2-4F8F-AD40-0EE6A9706A0C
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_STREAM, D3D11_VIDEO_PROCESSOR_STREAM structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_STREAM, mf.d3d11_video_processor_stream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: D3D11_VIDEO_PROCESSOR_STREAM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_PROCESSOR_STREAM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_PROCESSOR_STREAM structure


## -description


Contains stream-level data for the <a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">ID3D11VideoContext::VideoProcessorBlt</a> method.




## -struct-fields




### -field Enable

Specifies whether this input stream is enabled. If the value is <b>TRUE</b>, the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451703">VideoProcessorBlt</a> method blits this stream to the output surface. Otherwise, this stream is not blitted. 

The maximum number of streams that can be enabled at one time is given in the <b>MaxInputStreams</b> member of the <a href="https://msdn.microsoft.com/EF79BE15-B92E-45C1-BC42-E89E06197C20">D3D11_VIDEO_PROCESSOR_CAPS</a> structure. 




### -field OutputIndex

The zero-based index number of the output frame.


### -field InputFrameOrField

The zero-based index number of the input frame or field.


### -field PastFrames

The number of past reference frames.


### -field FutureFrames

The number of future reference frames.


### -field ppPastSurfaces

A pointer to an array of <a href="https://msdn.microsoft.com/E76B9CBE-2584-4DBC-8EF4-E9DA105226B9">ID3D11VideoProcessorInputView</a> pointers, allocated by the caller. This array contains the past reference frames for the video processing operation. The number of elements in the array is equal to <b>PastFrames</b>.


### -field pInputSurface

A pointer to the <a href="https://msdn.microsoft.com/E76B9CBE-2584-4DBC-8EF4-E9DA105226B9">ID3D11VideoProcessorInputView</a> interface of the surface that contains the current input frame.




### -field ppFutureSurfaces

A pointer to an array of <a href="https://msdn.microsoft.com/E76B9CBE-2584-4DBC-8EF4-E9DA105226B9">ID3D11VideoProcessorInputView</a> pointers, allocated by the caller. This array contains the future reference frames for the video processing operation. The number of elements in the array is equal to <b>FutureFrames</b>.


### -field ppPastSurfacesRight

If the stereo 3D format is <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b>, this member points to an array that contains the past reference frames for the right view. The number of elements in the array is equal to <b>PastFrames</b>.

For any other stereo 3D format, set this member to <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/FAAE902A-622E-42D2-B332-CD4126A4182E">ID3D11VideoContext::VideoProcessorSetStreamStereoFormat</a>.


### -field pInputSurfaceRight

If the stereo 3D format is <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b>, this member contains a pointer to the current input frame for the right view. 

For any other stereo 3D format, set this member to <b>NULL</b>. 


### -field ppFutureSurfacesRight

If the stereo 3D format is <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b>, this member points to an array that contains the future reference frames for the right view. The number of elements in the array is equal to <b>FutureFrames</b>.

For any other stereo 3D format, set this member to <b>NULL</b>. 


## -remarks



If the stereo 3D format is <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b>, the <b>ppPastSurfaces</b>, <b>pInputSurface</b>, and <b>ppFutureSurfaces</b> members contain the left view.




## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">ID3D11VideoContext::VideoProcessorBlt</a>
 

 

