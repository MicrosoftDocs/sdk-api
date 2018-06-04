---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# D3D11_VIDEO_PROCESSOR_STEREO_FORMAT enumeration


## -description


Specifies the layout in memory of a stereo 3D video frame.


## -enum-fields




### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO

The sample does not contain stereo data.  If the stereo format is not specified, this value is the default.


### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_HORIZONTAL

Frame 0 and frame 1 are packed side-by-side, as shown in the following diagram.

<img alt="Side-by-side packing" src="images/dxgistereo3d02.png"/>

All drivers that support stereo video must support this format.


### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_VERTICAL

Frame 0 and frame 1 are packed top-to-bottom, as shown in the following diagram.

<img alt="Top-to-bottom packing" src="images/dxgistereo3d01.png"/>

All drivers that support stereo video must support this format.


### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE

Frame 0 and frame 1 are placed in separate resources or in separate texture array elements within the same resource.

All drivers that support stereo video must support this format.


### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET

The sample contains non-stereo data. However, the driver should create a left/right output of this sample using a specified offset.  The offset is specified in the <i>MonoOffset</i> parameter of the <a href="https://msdn.microsoft.com/FAAE902A-622E-42D2-B332-CD4126A4182E">ID3D11VideoContext::VideoProcessorSetStreamStereoFormat</a> method. 

This format is primarily intended for subtitles and other subpicture data, where the entire sample is presented on the same plane.

Support for this stereo format is optional.


### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_ROW_INTERLEAVED

Frame 0 and frame 1 are packed into interleaved rows, as shown in the following diagram.

<img alt="Interleaved rows" src="images/dxgistereo3d03.png"/>

Support for this stereo format is optional.


### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_COLUMN_INTERLEAVED

Frame 0 and frame 1 are packed into interleaved columns, as shown in the following diagram.

<img alt="Interleaved columns" src="images/dxgistereo3d04.png"/>

Support for this stereo format is optional.


### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_CHECKERBOARD

Frame 0 and frame 1 are packed in a checkerboard format, as shown in the following diagram.

<img alt="Checkerboard packing" src="images/dxgistereo3d05.png"/>

Support for this stereo format is optional.


## -remarks



This enumeration designates the two stereo views as "frame 0" and "frame 1". The <i>LeftViewFrame0</i> parameter of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439817">VideoProcessorSetStreamStereoFormat</a> method specifies which view is the left view, and which is the right view.

For packed formats, if the source rectangle clips part of the surface, the driver interprets the rectangle in logical coordinates relative to the stereo view,  rather than absolute pixel coordinates. The result is that frame 0 and frame 1 are clipped proportionately.

To query whether the device supports stereo 3D video, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check for the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_STEREO</b> flag in the <b>FeatureCaps</b> member of the <a href="https://msdn.microsoft.com/EF79BE15-B92E-45C1-BC42-E89E06197C20">D3D11_VIDEO_PROCESSOR_CAPS</a> structure. If this capability flag is present, it means that the driver supports all of the stereo formats that are not  listed as optional. To find out which optional formats are supported, call <b>GetVideoProcessorCaps</b> and check the <b>StereoCaps</b> member of the structure.




## -see-also




<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>



<a href="https://msdn.microsoft.com/FAAE902A-622E-42D2-B332-CD4126A4182E">ID3D11VideoContext::VideoProcessorSetStreamStereoFormat</a>
 

 

