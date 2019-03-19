---
UID: NS:amvideo.tagVIDEOINFOHEADER
title: VIDEOINFOHEADER (amvideo.h)
author: windows-sdk-content
description: The VIDEOINFOHEADER structure describes the bitmap and color information for a video image.
old-location: dshow\videoinfoheader.htm
tech.root: DirectShow
ms.assetid: a175592b-0dc1-4001-b52f-785407965932
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VIDEOINFOHEADER, VIDEOINFOHEADER structure [DirectShow], VIDEOINFOHEADERStructure, amvideo/VIDEOINFOHEADER, dshow.videoinfoheader, tagVIDEOINFOHEADER
ms.topic: struct
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amvideo.h
api_name:
 - VIDEOINFOHEADER
product: Windows
targetos: Windows
req.typenames: VIDEOINFOHEADER
req.redist: 
---

# VIDEOINFOHEADER structure


## -description



The <b>VIDEOINFOHEADER</b> structure describes the bitmap and color information for a video image.




## -struct-fields




### -field rcSource

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the source video window. This structure can be a clipping rectangle, to select a portion of the source video stream.


### -field rcTarget

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the destination video window.


### -field dwBitRate

Approximate data rate of the video stream, in bits per second.


### -field dwBitErrorRate

Data error rate, in bit errors per second.


### -field AvgTimePerFrame

The desired average display time of the video frames, in 100-nanosecond units. The actual time per frame may be longer. See Remarks.


### -field bmiHeader


<a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure that contains color and dimension information for the video image bitmap. If the format block contains a color table or color masks, they immediately follow the <b>bmiHeader</b> member. You can get the first color entry by casting the address of member to a <b>BITMAPINFO</b> pointer.

When used inside a <b>VIDEOINFOHEADER</b> structure, the semantics of the <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure differ slightly from how the structure is used in GDI. For more information, refer to the topic <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER Structure</a>.


## -remarks



For information about using the <b>rcSource</b> and <b>rcTarget</b> members, see <a href="https://msdn.microsoft.com/fdddbffb-c44f-4364-9e2e-b721ba39c74f">Source and Target Rectangles in Video Renderers</a>.

<h3><a id="Frame_Rates"></a><a id="frame_rates"></a><a id="FRAME_RATES"></a>Frame Rates</h3>
The value of <b>AvgTimePerFrame</b> is usually set by the source filter, which obtains the value from the media stream. This value can be used to calculate the authored frame rate, which is the intended frame rate for the video to be rendered. During playback, the system may not be able to render the stream at the authored rate, so the actual frame rate may be less. This can happen if the machine's resources become over-committed. Also, the monitor's refresh rate can interfere with the playback rate of the video. For example, if the intended rate is 60,000/1001 (NTSC TV) and the monitor's refresh rate is 60Hz, the intended rate and the actual rate will never match. To retrieve the actual frame rate achieved during playback, use the <a href="https://msdn.microsoft.com/en-us/library/Dd376916(v=VS.85).aspx">IQualProp::get_AvgFrameRate</a> method on the video renderer.

During playback, applications can retrieve the authored frame rate as follows: 

<ul>
<li>If the old <a href="https://msdn.microsoft.com/7719ed9d-e3b9-4c84-b587-4e120b5cabf8">Video Renderer</a> filter is rendering, call the <a href="https://msdn.microsoft.com/en-us/library/Dd389575(v=VS.85).aspx">IBasicVideo::get_AvgTimePerFrame</a> method.</li>
<li>If the Video Mixing Renderer (VMR) is rendering, call <a href="https://msdn.microsoft.com/en-us/library/Dd390422(v=VS.85).aspx">IPin::ConnectionMediaType</a> on the input pin and examine the format block. The VMR supports multiple input streams, and they are not required to have the same frame rates.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

