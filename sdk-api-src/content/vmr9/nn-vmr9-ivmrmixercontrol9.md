---
UID: NN:vmr9.IVMRMixerControl9
title: IVMRMixerControl9 (vmr9.h)
description: The IVMRMixerControl9 interface enables an application to manipulate the incoming video streams on the Video Mixing Renderer Filter 9 (VMR-9). This interface is intended for use by applications only; it should not be used by upstream filters.
old-location: dshow\ivmrmixercontrol9.htm
tech.root: DirectShow
ms.assetid: f311303a-8270-40b6-8153-e0bd8b232c69
ms.date: 12/05/2018
ms.keywords: IVMRMixerControl9, IVMRMixerControl9 interface [DirectShow], IVMRMixerControl9 interface [DirectShow],described, IVMRMixerControl9Interface, dshow.ivmrmixercontrol9, vmr9/IVMRMixerControl9
f1_keywords:
- vmr9/IVMRMixerControl9
dev_langs:
- c++
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
- IVMRMixerControl9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRMixerControl9 interface


## -description



The <b>IVMRMixerControl9</b> interface enables an application to manipulate the incoming video streams on the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). This interface is intended for use by applications only; it should not be used by upstream filters.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRMixerControl9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRMixerControl9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRMixerControl9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-getalpha">GetAlpha</a>
</td>
<td align="left" width="63%">
Retrieves the constant alpha value that is applied to this video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-getbackgroundclr">GetBackgroundClr</a>
</td>
<td align="left" width="63%">
Retrieves the background color of the output rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-getmixingprefs">GetMixingPrefs</a>
</td>
<td align="left" width="63%">
Retrieves the mixing preferences for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-getoutputrect">GetOutputRect</a>
</td>
<td align="left" width="63%">
Retrieves the position of this stream's video rectangle within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-getprocampcontrol">GetProcAmpControl</a>
</td>
<td align="left" width="63%">
Retrieves the current image adjustment settings, such as brightness, contrast, hue, and saturation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-getprocampcontrolrange">GetProcAmpControlRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for an image adjustment setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-getzorder">GetZOrder</a>
</td>
<td align="left" width="63%">
Retrieves this video stream's position in the Z-order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-setalpha">SetAlpha</a>
</td>
<td align="left" width="63%">
Sets a constant alpha value that is applied to this video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-setbackgroundclr">SetBackgroundClr</a>
</td>
<td align="left" width="63%">
Sets the background color of the output rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs">SetMixingPrefs</a>
</td>
<td align="left" width="63%">
Sets the mixing preferences for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-setoutputrect">SetOutputRect</a>
</td>
<td align="left" width="63%">
Sets the position of this stream within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-setprocampcontrol">SetProcAmpControl</a>
</td>
<td align="left" width="63%">
Sets the image adjustment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-setzorder">SetZOrder</a>
</td>
<td align="left" width="63%">
Sets this video stream's position in the Z-order.

</td>
</tr>
</table> 


## -remarks



The VMR-9 supports this interface in mixing mode only. To enable mixing mode, call <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams">IVMRFilterConfig9::SetNumberOfStreams</a>. Otherwise, <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> returns <b>E_NOINTERFACE</b>. 

Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

