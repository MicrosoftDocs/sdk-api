---
UID: NN:strmif.IAMVideoControl
title: IAMVideoControl (strmif.h)

description: The IAMVideoControl interface controls certain video capture operations such as enumerating available frame rates and image orientation.
old-location: dshow\iamvideocontrol.htm
tech.root: DirectShow
ms.assetid: bd114977-c76c-4429-a835-98601b350a93

ms.date: 12/05/2018
ms.keywords: IAMVideoControl, IAMVideoControl interface [DirectShow], IAMVideoControl interface [DirectShow],described, IAMVideoControlInterface, dshow.iamvideocontrol, strmif/IAMVideoControl
ms.topic: interface
f1_keywords: 
 - "strmif/IAMVideoControl"
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
 - IAMVideoControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoControl interface


## -description



The <b>IAMVideoControl</b> interface controls certain video capture operations such as enumerating available frame rates and image orientation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVideoControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVideoControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocontrol-getcaps">GetCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the underlying hardware.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocontrol-getcurrentactualframerate">GetCurrentActualFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the actual frame rate at which the device is streaming. This method is used with devices, such as the Universal Serial Bus (USB) or cameras that use the IEEE 1394 serial standard, where the maximum frame rate can be limited by bandwidth availability. This is only available during video streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocontrol-getframeratelist">GetFrameRateList</a>
</td>
<td align="left" width="63%">
Retrieves a list of available frame rates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocontrol-getmaxavailableframerate">GetMaxAvailableFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the maximum frame rate currently available based on bus bandwidth usage for connections such as USB and IEEE 1394 camera devices where the maximum frame rate can be limited by bandwidth availability.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocontrol-getmode">GetMode</a>
</td>
<td align="left" width="63%">
Retrieves the video control mode of operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocontrol-setmode">SetMode</a>
</td>
<td align="left" width="63%">
Sets the video control mode of operation.

</td>
</tr>
</table> 


## -remarks



For Windows Driver Model (WDM) devices, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://docs.microsoft.com/windows-hardware/drivers/stream/propsetid-vidcap-videocontrol">PROPSETID_VIDCAP_VIDEOCONTROL</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

