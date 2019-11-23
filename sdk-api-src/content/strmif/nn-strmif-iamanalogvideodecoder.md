---
UID: NN:strmif.IAMAnalogVideoDecoder
title: IAMAnalogVideoDecoder (strmif.h)

description: The IAMAnalogVideoDecoder interface sets and retrieves information about the analog-to-digital conversion process in a video capture filter.The WDM Video Capture filter exposes this interface if the device is an analog video capture device.
old-location: dshow\iamanalogvideodecoder.htm
tech.root: DirectShow
ms.assetid: 81d43941-7c81-4220-915f-0b373a7455e5

ms.date: 12/05/2018
ms.keywords: IAMAnalogVideoDecoder, IAMAnalogVideoDecoder interface [DirectShow], IAMAnalogVideoDecoder interface [DirectShow],described, IAMAnalogVideoDecoderInterface, dshow.iamanalogvideodecoder, strmif/IAMAnalogVideoDecoder
ms.topic: interface
f1_keywords: 
 - "strmif/IAMAnalogVideoDecoder"
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
 - IAMAnalogVideoDecoder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMAnalogVideoDecoder interface


## -description



The <b>IAMAnalogVideoDecoder</b> interface sets and retrieves information about the analog-to-digital conversion process in a video capture filter.

The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture</a> filter exposes this interface if the device is an analog video capture device. Applications can use this interface to control aspects of the analog decoding process, such as the analog video format and the horizontal sync lock.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMAnalogVideoDecoder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMAnalogVideoDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMAnalogVideoDecoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideodecoder-get_availabletvformats">get_AvailableTVFormats</a>
</td>
<td align="left" width="63%">
Retrieves the analog video formats that the decoder supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideodecoder-get_horizontallocked">get_HorizontalLocked</a>
</td>
<td align="left" width="63%">
Determines whether the horizontal sync is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideodecoder-get_numberoflines">get_NumberOfLines</a>
</td>
<td align="left" width="63%">
Retrieves the number of scan lines in the video signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideodecoder-get_outputenable">get_OutputEnable</a>
</td>
<td align="left" width="63%">
Determines whether the video port bus is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideodecoder-get_tvformat">get_TVFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current analog video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideodecoder-get_vcrhorizontallocking">get_VCRHorizontalLocking</a>
</td>
<td align="left" width="63%">
Indicates whether the decoder is expecting video from a tape source or a broadcast source

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideodecoder-put_outputenable">put_OutputEnable</a>
</td>
<td align="left" width="63%">
Enables or disables the video port bus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideodecoder-put_tvformat">put_TVFormat</a>
</td>
<td align="left" width="63%">
Sets the analog video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamanalogvideodecoder-put_vcrhorizontallocking">put_VCRHorizontalLocking</a>
</td>
<td align="left" width="63%">
Specifies whether the video is a tape source or a broadcast source.

</td>
</tr>
</table> 


## -remarks



For Windows Driver Model (WDM) devices, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://docs.microsoft.com/windows-hardware/drivers/stream/propsetid-vidcap-videodecoder">PROPSETID_VIDCAP_VIDEODECODER</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

