---
UID: NN:videoacc.IAMVideoAcceleratorNotify
title: IAMVideoAcceleratorNotify (videoacc.h)
author: windows-sdk-content
description: The IAMVideoAcceleratorNotify interface is a callback interface used in conjunction with the IAMVideoAccelerator interface.
old-location: dshow\iamvideoacceleratornotify.htm
tech.root: DirectShow
ms.assetid: 7fd0290c-8fd6-4af6-b510-7a87bc7937de
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMVideoAcceleratorNotify, IAMVideoAcceleratorNotify interface [DirectShow], IAMVideoAcceleratorNotify interface [DirectShow],described, IAMVideoAcceleratorNotifyInterface, dshow.iamvideoacceleratornotify, videoacc/IAMVideoAcceleratorNotify
ms.topic: interface
f1_keywords: 
 - "videoacc/IAMVideoAcceleratorNotify"
req.header: videoacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoAcceleratorNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoAcceleratorNotify interface


## -description


The <b>IAMVideoAcceleratorNotify</b> interface is a callback interface used in conjunction with the <a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator</a> interface. It enables the video renderer filter to communicate with the video decoder when configuring 
        
      DirectX Video Acceleration (DXVA) decoding.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoAcceleratorNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVideoAcceleratorNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVideoAcceleratorNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata">GetCreateVideoAcceleratorData</a>
</td>
<td align="left" width="63%">
Gets information needed to create a video accelerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo">GetUncompSurfacesInfo</a>
</td>
<td align="left" width="63%">
Queries the decoder for the number of uncompressed surfaces to allocate and the pixel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo">SetUncompSurfacesInfo</a>
</td>
<td align="left" width="63%">
Notifies the decoder of how many uncompressed surfaces were created.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-reference">DirectShow Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>
 

 

