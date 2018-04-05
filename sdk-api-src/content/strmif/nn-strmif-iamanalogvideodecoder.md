---
UID: NN:strmif.IAMAnalogVideoDecoder
title: IAMAnalogVideoDecoder
author: windows-driver-content
description: The IAMAnalogVideoDecoder interface sets and retrieves information about the analog-to-digital conversion process in a video capture filter.The WDM Video Capture filter exposes this interface if the device is an analog video capture device.
old-location: dshow\iamanalogvideodecoder.htm
old-project: DirectShow
ms.assetid: 81d43941-7c81-4220-915f-0b373a7455e5
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IAMAnalogVideoDecoder, IAMAnalogVideoDecoder interface [DirectShow], IAMAnalogVideoDecoder interface [DirectShow], described, IAMAnalogVideoDecoderInterface, dshow.iamanalogvideodecoder, strmif/IAMAnalogVideoDecoder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMAnalogVideoDecoder
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAnalogVideoDecoder interface


## -description



The <b>IAMAnalogVideoDecoder</b> interface sets and retrieves information about the analog-to-digital conversion process in a video capture filter.

The <a href="https://msdn.microsoft.com/97432b99-e89b-4d69-963d-a959f887e580">WDM Video Capture</a> filter exposes this interface if the device is an analog video capture device. Applications can use this interface to control aspects of the analog decoding process, such as the analog video format and the horizontal sync lock.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMAnalogVideoDecoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMAnalogVideoDecoder</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/651f902f-de27-4185-b368-ce2cbf12cfae">get_AvailableTVFormats</a>
</td>
<td align="left" width="63%">
Retrieves the analog video formats that the decoder supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3923440-8770-42f1-a8f3-afa2e8a512d5">get_HorizontalLocked</a>
</td>
<td align="left" width="63%">
Determines whether the horizontal sync is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1c30230-bd47-4bdb-a89a-332c4da7cc00">get_NumberOfLines</a>
</td>
<td align="left" width="63%">
Retrieves the number of scan lines in the video signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2379079d-3852-45c7-a290-b3a33ea8af1a">get_OutputEnable</a>
</td>
<td align="left" width="63%">
Determines whether the video port bus is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8973281f-2037-487f-9e86-8c7ceca75b23">get_TVFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current analog video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b527578-1840-4cb1-b94b-9be27b40fcf4">get_VCRHorizontalLocking</a>
</td>
<td align="left" width="63%">
Indicates whether the decoder is expecting video from a tape source or a broadcast source

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93163db3-ea9a-4383-b382-7d574ef24dfc">put_OutputEnable</a>
</td>
<td align="left" width="63%">
Enables or disables the video port bus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea1522a0-1f00-40c4-9e50-3638495e209c">put_TVFormat</a>
</td>
<td align="left" width="63%">
Sets the analog video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b215f8b-dfd9-40cf-a392-7cc42b17b214">put_VCRHorizontalLocking</a>
</td>
<td align="left" width="63%">
Specifies whether the video is a tape source or a broadcast source.

</td>
</tr>
</table> 


## -remarks



For Windows Driver Model (WDM) devices, the <a href="https://msdn.microsoft.com/97432b99-e89b-4d69-963d-a959f887e580">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568121">PROPSETID_VIDCAP_VIDEODECODER</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

