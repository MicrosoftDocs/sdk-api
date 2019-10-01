---
UID: NN:segment.IMSVidVideoRenderer
title: IMSVidVideoRenderer (segment.h)
author: windows-sdk-content
description: The IMSVidVideoRenderer interface represents a video renderer device. The MSVidVideoRenderer object exposes this interface.This interface provides access to the Video Mixing Renderer (VMR) filter.
old-location: mstv\imsvidvideorenderer.htm
tech.root: mstv
ms.assetid: 27eb53f8-ece8-43eb-8f94-b3d2d91548ad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer, IMSVidVideoRenderer interface [Microsoft TV Technologies], IMSVidVideoRenderer interface [Microsoft TV Technologies],described, IMSVidVideoRendererInterface, mstv.imsvidvideorenderer, segment/IMSVidVideoRenderer
ms.topic: interface
f1_keywords: 
 - "segment/IMSVidVideoRenderer"
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidVideoRenderer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidVideoRenderer interface


## -description



The <b>IMSVidVideoRenderer</b> interface represents a video renderer device. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695138(v=vs.85)">MSVidVideoRenderer</a> object exposes this interface.

This interface provides access to the Video Mixing Renderer (VMR) filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidVideoRenderer</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>. <b>IMSVidVideoRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidVideoRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-capture">Capture</a>
</td>
<td align="left" width="63%">
Captures the video frame that is currently being rendered by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get__customcompositor">get__CustomCompositor</a>
</td>
<td align="left" width="63%">
Retrieves the VMR's current image compositor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get__customcompositorclass">get__CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Retrieves the class identifier (CLSID) of the VMR's current image compositor, as a <b>GUID</b>

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get__mixerbitmap">get__MixerBitmap</a>
</td>
<td align="left" width="63%">
Retrieves the VMR's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrmixerbitmap">IVMRMixerBitmap</a> interface, which controls how the VMR mixes a static bitmap

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_availablesourcerect">get_AvailableSourceRect</a>
</td>
<td align="left" width="63%">
Retrieves the size of the native video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_clippedsourcerect">get_ClippedSourceRect</a>
</td>
<td align="left" width="63%">
Retrieves the clipping rectangle on the video source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_customcompositorclass">get_CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of the VMR's current image compositor, as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_decimateinput">get_DecimateInput</a>
</td>
<td align="left" width="63%">
Indicates whether the VMR will decimate the video (that is, reduce the native video size) before processing it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_framespersecond">get_FramesPerSecond</a>
</td>
<td align="left" width="63%">
Retrieves the current frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_maxvidrect">get_MaxVidRect</a>
</td>
<td align="left" width="63%">
Retrieves the maximum ideal size of the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_minvidrect">get_MinVidRect</a>
</td>
<td align="left" width="63%">
Retrieves the minimum ideal size of the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmap">get_MixerBitmap</a>
</td>
<td align="left" width="63%">
Retrieves the static bitmap image, as an <b>IPictureDisp</b> type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmapopacity">get_MixerBitmapOpacity</a>
</td>
<td align="left" width="63%">
Retrieves the opacity of the static bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmappositionrect">get_MixerBitmapPositionRect</a>
</td>
<td align="left" width="63%">
Retrieves the position of the static bitmap image, relative to the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_overscan">get_OverScan</a>
</td>
<td align="left" width="63%">
Retrieves the amount of clipping to perform on all sides of the video frame, in order to cut off random video noise.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_sourcesize">get_SourceSize</a>
</td>
<td align="left" width="63%">
Retrieves the type of clipping to apply to the video rectangle, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_usingoverlay">get_UsingOverlay</a>
</td>
<td align="left" width="63%">
Queries whether the VMR is using the hardware overlay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put__customcompositor">put__CustomCompositor</a>
</td>
<td align="left" width="63%">
Specifies a custom image compositor for the VMR to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put__customcompositorclass">put__CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Specifies the CLSID of a custom image compositor, as a <b>GUID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put__mixerbitmap">put__MixerBitmap</a>
</td>
<td align="left" width="63%">
Specifies the static bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_clippedsourcerect">put_ClippedSourceRect</a>
</td>
<td align="left" width="63%">
Specifies the clipping rectangle on the video source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_customcompositorclass">put_CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Specifies the CLSID of a custom image compositor, as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_decimateinput">put_DecimateInput</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will decimate the video (that is, reduce the native video size) before processing it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmap">put_MixerBitmap</a>
</td>
<td align="left" width="63%">
Specifies the static bitmap image, as an <b>IPictureDisp</b> type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmapopacity">put_MixerBitmapOpacity</a>
</td>
<td align="left" width="63%">
Specifies the opacity of the static bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmappositionrect">put_MixerBitmapPositionRect</a>
</td>
<td align="left" width="63%">
Specifies the position of the static bitmap image, relative to the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_overscan">put_OverScan</a>
</td>
<td align="left" width="63%">
Specifies the amount of clipping to perform on all sides of the video frame, in order to cut off random video noise.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_sourcesize">put_SourceSize</a>
</td>
<td align="left" width="63%">
Specifies the type of clipping to apply to the video rectangle, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_usingoverlay">put_UsingOverlay</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will use the hardware overlay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-setupmixerbitmap">SetupMixerBitmap</a>
</td>
<td align="left" width="63%">
Configures the VMR to display an alpha-blended bitmap on top of the video.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVideoRenderer)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

