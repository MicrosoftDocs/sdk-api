---
UID: NN:segment.IMSVidVideoRenderer
title: IMSVidVideoRenderer
author: windows-sdk-content
description: The IMSVidVideoRenderer interface represents a video renderer device. The MSVidVideoRenderer object exposes this interface.This interface provides access to the Video Mixing Renderer (VMR) filter.
old-location: mstv\imsvidvideorenderer.htm
tech.root: MSTV
ms.assetid: 27eb53f8-ece8-43eb-8f94-b3d2d91548ad
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidVideoRenderer, IMSVidVideoRenderer interface [Microsoft TV Technologies], IMSVidVideoRenderer interface [Microsoft TV Technologies],described, IMSVidVideoRendererInterface, mstv.imsvidvideorenderer, segment/IMSVidVideoRenderer
ms.prod: windows-hardware
ms.technology: windows-devices
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
<a href="https://msdn.microsoft.com/05287e53-a988-43cc-ac41-5024a217621a">Capture</a>
</td>
<td align="left" width="63%">
Captures the video frame that is currently being rendered by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cafdc512-2994-4374-9396-b0bb946bc490">get__CustomCompositor</a>
</td>
<td align="left" width="63%">
Retrieves the VMR's current image compositor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ac48bbb-a0d3-4c37-9f3e-4f4cc79b550b">get__CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Retrieves the class identifier (CLSID) of the VMR's current image compositor, as a <b>GUID</b>

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/714b8222-ab8b-4ece-8ae5-61bb41a7ed3c">get__MixerBitmap</a>
</td>
<td align="left" width="63%">
Retrieves the VMR's <a href="https://msdn.microsoft.com/ac7da3f9-2c17-4517-bb64-6b56257a65c3">IVMRMixerBitmap</a> interface, which controls how the VMR mixes a static bitmap

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33747e97-3e1c-4220-89c9-cc8310b77c4e">get_AvailableSourceRect</a>
</td>
<td align="left" width="63%">
Retrieves the size of the native video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d40d39d9-41a4-42e1-b0d0-4a6299fd1cff">get_ClippedSourceRect</a>
</td>
<td align="left" width="63%">
Retrieves the clipping rectangle on the video source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6ff1968-e891-432d-9271-f6d6a6a8a756">get_CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of the VMR's current image compositor, as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f533b85-175b-4381-b7a9-eac0d8e313ed">get_DecimateInput</a>
</td>
<td align="left" width="63%">
Indicates whether the VMR will decimate the video (that is, reduce the native video size) before processing it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94634499-748d-42d1-8d06-fb52d10d4656">get_FramesPerSecond</a>
</td>
<td align="left" width="63%">
Retrieves the current frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4c4b2da-0749-463c-aaa1-04d0d456327a">get_MaxVidRect</a>
</td>
<td align="left" width="63%">
Retrieves the maximum ideal size of the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e65f2b2-d479-429a-b5c7-8c5cbb6c833d">get_MinVidRect</a>
</td>
<td align="left" width="63%">
Retrieves the minimum ideal size of the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfcfab14-7084-4716-8955-574168cd3506">get_MixerBitmap</a>
</td>
<td align="left" width="63%">
Retrieves the static bitmap image, as an <b>IPictureDisp</b> type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/830eff1a-e70e-440c-81be-69058d14f314">get_MixerBitmapOpacity</a>
</td>
<td align="left" width="63%">
Retrieves the opacity of the static bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2270786-5289-4c41-898e-651ed881842b">get_MixerBitmapPositionRect</a>
</td>
<td align="left" width="63%">
Retrieves the position of the static bitmap image, relative to the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c4946e6-b25c-4e6a-b640-73982c0da871">get_OverScan</a>
</td>
<td align="left" width="63%">
Retrieves the amount of clipping to perform on all sides of the video frame, in order to cut off random video noise.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/312a2c1e-5332-4a2d-ada9-1dc8236f4170">get_SourceSize</a>
</td>
<td align="left" width="63%">
Retrieves the type of clipping to apply to the video rectangle, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd41cbcc-b8a8-4b08-9b25-399e366614ce">get_UsingOverlay</a>
</td>
<td align="left" width="63%">
Queries whether the VMR is using the hardware overlay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff99b253-20bc-4b8e-8624-ffcbb3b91857">put__CustomCompositor</a>
</td>
<td align="left" width="63%">
Specifies a custom image compositor for the VMR to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/031af4a5-6eed-44c9-9b0c-f472d709db66">put__CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Specifies the CLSID of a custom image compositor, as a <b>GUID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dd7b83e-6ed6-4c57-8a00-a4ed2c78840d">put__MixerBitmap</a>
</td>
<td align="left" width="63%">
Specifies the static bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c72d8134-ff6c-46b4-b567-35638aef53cd">put_ClippedSourceRect</a>
</td>
<td align="left" width="63%">
Specifies the clipping rectangle on the video source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/399a5151-b26a-4c33-9dd9-e7abb23cbd1c">put_CustomCompositorClass</a>
</td>
<td align="left" width="63%">
Specifies the CLSID of a custom image compositor, as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e048a572-3a96-4610-9266-0e97b5a09778">put_DecimateInput</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will decimate the video (that is, reduce the native video size) before processing it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa9d9bea-f711-42f1-a247-322036744c44">put_MixerBitmap</a>
</td>
<td align="left" width="63%">
Specifies the static bitmap image, as an <b>IPictureDisp</b> type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dba67ab-9522-48a3-be09-8ed8c27bffee">put_MixerBitmapOpacity</a>
</td>
<td align="left" width="63%">
Specifies the opacity of the static bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05542d75-1723-4581-ac8b-6a577e0085cb">put_MixerBitmapPositionRect</a>
</td>
<td align="left" width="63%">
Specifies the position of the static bitmap image, relative to the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/141df99b-4fc7-439c-953e-1fa1c544258e">put_OverScan</a>
</td>
<td align="left" width="63%">
Specifies the amount of clipping to perform on all sides of the video frame, in order to cut off random video noise.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c792f064-a137-4872-8c79-6e924b6023f0">put_SourceSize</a>
</td>
<td align="left" width="63%">
Specifies the type of clipping to apply to the video rectangle, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee7a5c92-bdae-4b67-9b2b-5fb4ae3a8fd7">put_UsingOverlay</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will use the hardware overlay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a91561e3-469b-412a-b5ab-af2a5a0855a6">SetupMixerBitmap</a>
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
 

 

