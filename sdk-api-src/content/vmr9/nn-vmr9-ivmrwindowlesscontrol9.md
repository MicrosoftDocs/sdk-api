---
UID: NN:vmr9.IVMRWindowlessControl9
title: IVMRWindowlessControl9 (vmr9.h)
description: The IVMRWindowlessControl9 interface controls how the Video Mixing Renderer Filter 9 (VMR-9) renders a video stream within a container window.
old-location: dshow\ivmrwindowlesscontrol9.htm
tech.root: DirectShow
ms.assetid: 9db99c31-65b5-4ff1-9c0d-22140a3687e8
ms.date: 12/05/2018
ms.keywords: IVMRWindowlessControl9, IVMRWindowlessControl9 interface [DirectShow], IVMRWindowlessControl9 interface [DirectShow],described, IVMRWindowlessControl9Interface, dshow.ivmrwindowlesscontrol9, vmr9/IVMRWindowlessControl9
ms.topic: interface
f1_keywords:
- vmr9/IVMRWindowlessControl9
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
- IVMRWindowlessControl9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl9 interface


## -description



The <b>IVMRWindowlessControl9</b> interface controls how the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9) renders a video stream within a container window. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRWindowlessControl9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRWindowlessControl9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRWindowlessControl9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged">DisplayModeChanged</a>
</td>
<td align="left" width="63%">
Informs the VMR that a <a href="https://docs.microsoft.com/windows/desktop/gdi/wm-displaychange">WM_DISPLAYCHANGE</a> message has been received by the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getaspectratiomode">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Retrieves the current aspect ratio display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getbordercolor">GetBorderColor</a>
</td>
<td align="left" width="63%">
Retrieves the current border color used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getcurrentimage">GetCurrentImage</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the current image being displayed by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getmaxidealvideosize">GetMaxIdealVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum video size that the VMR can display without incurring significant performance or image quality degradation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getminidealvideosize">GetMinIdealVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the minimum video size that the VMR can display without incurring significant performance or image quality degradation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize">GetNativeVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the un-stretched video size and aspect ratio of the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getvideoposition">GetVideoPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current source and destination rectangles used to display the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo">RepaintVideo</a>
</td>
<td align="left" width="63%">
Repaints the current video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Sets the current aspect ratio display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-setbordercolor">SetBorderColor</a>
</td>
<td align="left" width="63%">
Sets the border color to be used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow">SetVideoClippingWindow</a>
</td>
<td align="left" width="63%">
Specifies the container window that video should be clipped to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition">SetVideoPosition</a>
</td>
<td align="left" width="63%">
Sets the source and destination rectangles for the video.

</td>
</tr>
</table> 


## -remarks



The VMR-9 supports this interface in windowless and renderless modes only. In windowed mode, <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> returns <b>E_NOINTERFACE</b>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/vmr-modes-of-operation">VMR Modes of Operation</a>.

Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

