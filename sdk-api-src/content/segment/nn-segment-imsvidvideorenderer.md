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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer interface


## -description



The <b>IMSVidVideoRenderer</b> interface represents a video renderer device. The <a href="https://msdn.microsoft.com/ffb9566f-1c03-4aba-a9ce-a47e42894ca0">MSVidVideoRenderer</a> object exposes this interface.

This interface provides access to the Video Mixing Renderer (VMR) filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidVideoRenderer</b> interface inherits from <a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a>. <b>IMSVidVideoRenderer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd694731(v=VS.85).aspx">Capture</a>
</td>
<td align="left" width="63%">
Captures the video frame that is currently being rendered by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694745(v=VS.85).aspx">get__CustomCompositor</a>
</td>
<td align="left" width="63%">
Retrieves the VMR's current image compositor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694746(v=VS.85).aspx">get__CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Retrieves the class identifier (CLSID) of the VMR's current image compositor, as a <b>GUID</b>

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694747(v=VS.85).aspx">get__MixerBitmap</a>
</td>
<td align="left" width="63%">
Retrieves the VMR's <a href="https://msdn.microsoft.com/en-us/library/Dd390448(v=VS.85).aspx">IVMRMixerBitmap</a> interface, which controls how the VMR mixes a static bitmap

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694732(v=VS.85).aspx">get_AvailableSourceRect</a>
</td>
<td align="left" width="63%">
Retrieves the size of the native video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694733(v=VS.85).aspx">get_ClippedSourceRect</a>
</td>
<td align="left" width="63%">
Retrieves the clipping rectangle on the video source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694734(v=VS.85).aspx">get_CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of the VMR's current image compositor, as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694735(v=VS.85).aspx">get_DecimateInput</a>
</td>
<td align="left" width="63%">
Indicates whether the VMR will decimate the video (that is, reduce the native video size) before processing it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694736(v=VS.85).aspx">get_FramesPerSecond</a>
</td>
<td align="left" width="63%">
Retrieves the current frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694737(v=VS.85).aspx">get_MaxVidRect</a>
</td>
<td align="left" width="63%">
Retrieves the maximum ideal size of the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694738(v=VS.85).aspx">get_MinVidRect</a>
</td>
<td align="left" width="63%">
Retrieves the minimum ideal size of the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694739(v=VS.85).aspx">get_MixerBitmap</a>
</td>
<td align="left" width="63%">
Retrieves the static bitmap image, as an <b>IPictureDisp</b> type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694740(v=VS.85).aspx">get_MixerBitmapOpacity</a>
</td>
<td align="left" width="63%">
Retrieves the opacity of the static bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694741(v=VS.85).aspx">get_MixerBitmapPositionRect</a>
</td>
<td align="left" width="63%">
Retrieves the position of the static bitmap image, relative to the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694742(v=VS.85).aspx">get_OverScan</a>
</td>
<td align="left" width="63%">
Retrieves the amount of clipping to perform on all sides of the video frame, in order to cut off random video noise.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694743(v=VS.85).aspx">get_SourceSize</a>
</td>
<td align="left" width="63%">
Retrieves the type of clipping to apply to the video rectangle, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694744(v=VS.85).aspx">get_UsingOverlay</a>
</td>
<td align="left" width="63%">
Queries whether the VMR is using the hardware overlay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694757(v=VS.85).aspx">put__CustomCompositor</a>
</td>
<td align="left" width="63%">
Specifies a custom image compositor for the VMR to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694758(v=VS.85).aspx">put__CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Specifies the CLSID of a custom image compositor, as a <b>GUID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694759(v=VS.85).aspx">put__MixerBitmap</a>
</td>
<td align="left" width="63%">
Specifies the static bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694748(v=VS.85).aspx">put_ClippedSourceRect</a>
</td>
<td align="left" width="63%">
Specifies the clipping rectangle on the video source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694749(v=VS.85).aspx">put_CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Specifies the CLSID of a custom image compositor, as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694750(v=VS.85).aspx">put_DecimateInput</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will decimate the video (that is, reduce the native video size) before processing it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694751(v=VS.85).aspx">put_MixerBitmap</a>
</td>
<td align="left" width="63%">
Specifies the static bitmap image, as an <b>IPictureDisp</b> type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694752(v=VS.85).aspx">put_MixerBitmapOpacity</a>
</td>
<td align="left" width="63%">
Specifies the opacity of the static bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694753(v=VS.85).aspx">put_MixerBitmapPositionRect</a>
</td>
<td align="left" width="63%">
Specifies the position of the static bitmap image, relative to the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694754(v=VS.85).aspx">put_OverScan</a>
</td>
<td align="left" width="63%">
Specifies the amount of clipping to perform on all sides of the video frame, in order to cut off random video noise.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694755(v=VS.85).aspx">put_SourceSize</a>
</td>
<td align="left" width="63%">
Specifies the type of clipping to apply to the video rectangle, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694756(v=VS.85).aspx">put_UsingOverlay</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will use the hardware overlay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694760(v=VS.85).aspx">SetupMixerBitmap</a>
</td>
<td align="left" width="63%">
Configures the VMR to display an alpha-blended bitmap on top of the video.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVideoRenderer)</code>.




## -see-also




<a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

