---
UID: NN:mfidl.IMFVideoProcessorControl2
title: IMFVideoProcessorControl2 (mfidl.h)
description: Configures the Video Processor MFT.
old-location: mf\imfvideoprocessorcontrol2.htm
tech.root: medfound
ms.assetid: FE314254-AAE4-482E-A7AE-28B2591E0060
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessorControl2, IMFVideoProcessorControl2 interface [Media Foundation], IMFVideoProcessorControl2 interface [Media Foundation],described, mf.imfvideoprocessorcontrol2, mfidl/IMFVideoProcessorControl2
ms.topic: interface
f1_keywords:
- mfidl/IMFVideoProcessorControl2
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfidl.idl
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
- mfidl.h
api_name:
- IMFVideoProcessorControl2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoProcessorControl2 interface


## -description


Configures the <a href="https://docs.microsoft.com/windows/desktop/medfound/video-processor-mft">Video Processor MFT</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoProcessorControl2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol">IMFVideoProcessorControl</a>. <b>IMFVideoProcessorControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoProcessorControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol2-enablehardwareeffects">EnableHardwareEffects</a>
</td>
<td align="left" width="63%">
Enables effects that were implemented with <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">IDirectXVideoProcessor::VideoProcessorBlt</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol2-getsupportedhardwareeffects">GetSupportedHardwareEffects</a>
</td>
<td align="left" width="63%">
Returns the list of supported effects in the currently configured video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol2-setrotationoverride">SetRotationOverride</a>
</td>
<td align="left" width="63%">
Overrides the rotation operation that is performed in the video processor.

</td>
</tr>
</table> 


## -remarks



This interface controls how the <a href="https://docs.microsoft.com/windows/desktop/medfound/video-processor-mft">Video Processor MFT</a> generates output frames.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol">IMFVideoProcessorControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

