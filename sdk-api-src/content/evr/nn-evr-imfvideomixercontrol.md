---
UID: NN:evr.IMFVideoMixerControl
title: IMFVideoMixerControl
author: windows-sdk-content
description: Controls how the Enhanced Video Renderer (EVR) mixes video substreams.
old-location: mf\imfvideomixercontrol.htm
tech.root: medfound
ms.assetid: 8b5f54e3-c6da-4201-857a-9c718ad911db
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 8b5f54e3-c6da-4201-857a-9c718ad911db, IMFVideoMixerControl, IMFVideoMixerControl interface [Media Foundation], IMFVideoMixerControl interface [Media Foundation],described, evr/IMFVideoMixerControl, mf.imfvideomixercontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: evr.h
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
 - IMFVideoMixerControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoMixerControl interface


## -description


Controls how the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR) mixes video substreams. Applications can use this interface to control video mixing during playback.

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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoMixerControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoMixerControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoMixerControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6de631cd-f85e-4f53-b14c-8ca3cd65b719">GetStreamOutputRect</a>
</td>
<td align="left" width="63%">
Retrieves the position of a video stream within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e0ba97c-c960-4e26-a89c-ea1a4e91e907">GetStreamZOrder</a>
</td>
<td align="left" width="63%">
Retrieves the z-order of a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7075b8cf-2106-4b13-abc7-8aedae18bb62">SetStreamOutputRect</a>
</td>
<td align="left" width="63%">
Sets the position of a video stream within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6187724a-6345-4feb-90a0-097b6d21180f">SetStreamZOrder</a>
</td>
<td align="left" width="63%">
Sets the z-order of a video stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

