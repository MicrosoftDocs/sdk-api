---
UID: NN:wmdxva.IWMCodecAMVideoAccelerator
title: IWMCodecAMVideoAccelerator (wmdxva.h)
description: This interface is exposed by the Windows Media Decoder DMO and is called by a media player source filter to set up the various connections required to enable DirectX&#174; video acceleration (VA) for decoding of Windows Media-based video content.
old-location: wmformat\iwmcodecamvideoaccelerator.htm
tech.root: wmformat
ms.assetid: 48cfc4d1-4b79-47a5-9cc9-a1f19d2c0123
ms.date: 12/05/2018
ms.keywords: IWMCodecAMVideoAccelerator, IWMCodecAMVideoAccelerator interface [windows Media Format], IWMCodecAMVideoAccelerator interface [windows Media Format],described, IWMCodecAMVideoAcceleratorInterface, wmdxva/IWMCodecAMVideoAccelerator, wmformat.iwmcodecamvideoaccelerator
f1_keywords:
- wmdxva/IWMCodecAMVideoAccelerator
dev_langs:
- c++
req.header: wmdxva.h
req.include-header: 
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
- COM
api_location:
- wmdxva.h
api_name:
- IWMCodecAMVideoAccelerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMCodecAMVideoAccelerator interface


## -description



This interface is exposed by the Windows Media Decoder <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">DMO</a> and is called by a media player source filter to set up the various connections required to enable DirectX® video acceleration (VA) for decoding of Windows Media-based video content. A player obtains this interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderaccelerator-getcodecinterface">IWMReaderAccelerator::GetCodecInterface</a> method, which is exposed on the reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecAMVideoAccelerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCodecAMVideoAccelerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecAMVideoAccelerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdxva/nf-wmdxva-iwmcodecamvideoaccelerator-negotiateconnection">NegotiateConnection</a>
</td>
<td align="left" width="63%">
Called by the output pin on the player's source filter during the connection process when it has been given a DirectX VA media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdxva/nf-wmdxva-iwmcodecamvideoaccelerator-setacceleratorinterface">SetAcceleratorInterface</a>
</td>
<td align="left" width="63%">
Called by the output pin on the player's source filter to pass the VMR's <b>IAMVideoAccelerator</b> interface to the decoder DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdxva/nf-wmdxva-iwmcodecamvideoaccelerator-setplayernotify">SetPlayerNotify</a>
</td>
<td align="left" width="63%">
Called by the output pin on the source filter to provide the decoder DMO with the source filter's <b>IWMPlayerTimestampHook</b> interface to enable the filter to update the time stamps on the samples before they are delivered to the renderer.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>
 

 

