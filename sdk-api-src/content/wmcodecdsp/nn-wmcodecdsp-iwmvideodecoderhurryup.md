---
UID: NN:wmcodecdsp.IWMVideoDecoderHurryup
title: IWMVideoDecoderHurryup (wmcodecdsp.h)
author: windows-sdk-content
description: Controls the speed of the video decoder.
old-location: mf\iwmvideodecoderhurryupinterface.htm
tech.root: medfound
ms.assetid: 5e33be5f-5ce8-4f4f-94db-4be2dfcaeec0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMVideoDecoderHurryup, IWMVideoDecoderHurryup interface [Media Foundation], IWMVideoDecoderHurryup interface [Media Foundation],described, codecapi.iwmvideodecoderhurryupinterface, mf.iwmvideodecoderhurryup, mf.iwmvideodecoderhurryupinterface, wmcodecdsp/IWMVideoDecoderHurryup
ms.topic: interface
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - wmcodecdsp.h
api_name:
 - IWMVideoDecoderHurryup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMVideoDecoderHurryup interface


## -description



Controls the speed of the video decoder.



This interface is implemented by the video decoder objects. You can obtain a pointer to <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderhurryup">IWMVideoDecoderHurryup</a> by calling the <b>QueryInterface</b> method of any other interface of the decoder, such as <a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMVideoDecoderHurryup</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMVideoDecoderHurryup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMVideoDecoderHurryup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmvideodecoderhurryup-gethurryup">GetHurryup</a>
</td>
<td align="left" width="63%">
Retrieves the current speed mode of the video decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmvideodecoderhurryup-sethurryup">SetHurryup</a>
</td>
<td align="left" width="63%">
Sets the speed mode of the video decoder.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

