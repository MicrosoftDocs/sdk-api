---
UID: NN:evr9.IMFVideoMixerBitmap
title: IMFVideoMixerBitmap (evr9.h)
description: Alpha-blends a static bitmap image with the video displayed by the Enhanced Video Renderer (EVR).
old-location: mf\imfvideomixerbitmap.htm
tech.root: medfound
ms.assetid: 4da4bdb9-857b-40c9-b910-04a099a23ab5
ms.date: 12/05/2018
ms.keywords: 4da4bdb9-857b-40c9-b910-04a099a23ab5, IMFVideoMixerBitmap, IMFVideoMixerBitmap interface [Media Foundation], IMFVideoMixerBitmap interface [Media Foundation],described, evr9/IMFVideoMixerBitmap, mf.imfvideomixerbitmap
ms.topic: interface
f1_keywords:
- evr9/IMFVideoMixerBitmap
dev_langs:
- c++
req.header: evr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
api_name:
- IMFVideoMixerBitmap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoMixerBitmap interface


## -description


Alpha-blends a static bitmap image with the video displayed by the <a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR).

The EVR mixer implements this interface. To get a pointer to the interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier GUID is MR_VIDEO_MIXER_SERVICE. Call <b>GetService</b> on any of the following objects:
<ul>
<li>The <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a>, if the topology contains an instance of the EVR.
            </li>
<li>The EVR media sink.
            </li>
<li>The DirectShow EVR filter.
            </li>
<li>The EVR mixer.
            </li>
</ul>If you implement a custom mixer for the EVR, the mixer can optionally expose this interface as a service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoMixerBitmap</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoMixerBitmap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoMixerBitmap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-clearalphabitmap">ClearAlphaBitmap</a>
</td>
<td align="left" width="63%">
Removes the current bitmap and releases any resources associated with it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-getalphabitmapparameters">GetAlphaBitmapParameters</a>
</td>
<td align="left" width="63%">
Retrieves the current settings that the EVR uses to alpha-blend the bitmap with the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap">SetAlphaBitmap</a>
</td>
<td align="left" width="63%">
Sets a bitmap image for the EVR to alpha-blend with the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters">UpdateAlphaBitmapParameters</a>
</td>
<td align="left" width="63%">
Updates the current alpha-blending settings.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

