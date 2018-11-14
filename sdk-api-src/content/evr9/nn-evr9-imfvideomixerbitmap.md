---
UID: NN:evr9.IMFVideoMixerBitmap
title: IMFVideoMixerBitmap
author: windows-sdk-content
description: Alpha-blends a static bitmap image with the video displayed by the Enhanced Video Renderer (EVR).
old-location: mf\imfvideomixerbitmap.htm
tech.root: medfound
ms.assetid: 4da4bdb9-857b-40c9-b910-04a099a23ab5
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 4da4bdb9-857b-40c9-b910-04a099a23ab5, IMFVideoMixerBitmap, IMFVideoMixerBitmap interface [Media Foundation], IMFVideoMixerBitmap interface [Media Foundation],described, evr9/IMFVideoMixerBitmap, mf.imfvideomixerbitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoMixerBitmap interface


## -description


Alpha-blends a static bitmap image with the video displayed by the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR).

The EVR mixer implements this interface. To get a pointer to the interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a>. The service identifier GUID is MR_VIDEO_MIXER_SERVICE. Call <b>GetService</b> on any of the following objects:
<ul>
<li>The <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a>, if the topology contains an instance of the EVR.
            </li>
<li>The EVR media sink.
            </li>
<li>The DirectShow EVR filter.
            </li>
<li>The EVR mixer.
            </li>
</ul>If you implement a custom mixer for the EVR, the mixer can optionally expose this interface as a service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoMixerBitmap</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoMixerBitmap</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/79a0f24c-9388-4c64-885f-5d04e671669e">ClearAlphaBitmap</a>
</td>
<td align="left" width="63%">
Removes the current bitmap and releases any resources associated with it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0361e340-9de7-47f3-80fd-61d5e914d44e">GetAlphaBitmapParameters</a>
</td>
<td align="left" width="63%">
Retrieves the current settings that the EVR uses to alpha-blend the bitmap with the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a70e6734-bf49-4dea-8bf6-917b8465cc78">SetAlphaBitmap</a>
</td>
<td align="left" width="63%">
Sets a bitmap image for the EVR to alpha-blend with the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/369bf934-b0a0-44b2-bea2-e8575404d36d">UpdateAlphaBitmapParameters</a>
</td>
<td align="left" width="63%">
Updates the current alpha-blending settings.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

