---
UID: NN:strmif.IAMVideoProcAmp
title: IAMVideoProcAmp (strmif.h)
author: windows-sdk-content
description: The IAMVideoProcAmp interface adjusts the qualities of an incoming video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.The WDM Video Capture filter exposes this interface if the hardware supports image adjustment.
old-location: dshow\iamvideoprocamp.htm
tech.root: DirectShow
ms.assetid: 28c45790-2e5a-4acb-8a53-93f19c51dc6a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMVideoProcAmp, IAMVideoProcAmp interface [DirectShow], IAMVideoProcAmp interface [DirectShow],described, IAMVideoProcAmpInterface, dshow.iamvideoprocamp, strmif/IAMVideoProcAmp
ms.topic: interface
f1_keywords: 
 - "strmif/IAMVideoProcAmp"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMVideoProcAmp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoProcAmp interface


## -description



The <b>IAMVideoProcAmp</b> interface adjusts the qualities of an incoming video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.

The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture</a> filter exposes this interface if the hardware supports image adjustment.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoProcAmp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVideoProcAmp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVideoProcAmp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideoprocamp-get">Get</a>
</td>
<td align="left" width="63%">
Gets video quality for a specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideoprocamp-getrange">GetRange</a>
</td>
<td align="left" width="63%">
Gets the minimum, maximum, and default values for setting properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideoprocamp-set">Set</a>
</td>
<td align="left" width="63%">
Sets video quality for a specified property.

</td>
</tr>
</table> 


## -remarks



For Windows Driver Model (WDM) devices, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://docs.microsoft.com/windows-hardware/drivers/stream/propsetid-vidcap-videoprocamp">PROPSETID_VIDCAP_VIDEOPROCAMP</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

