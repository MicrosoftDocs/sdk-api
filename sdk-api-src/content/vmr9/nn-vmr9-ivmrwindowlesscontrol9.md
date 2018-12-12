---
UID: NN:vmr9.IVMRWindowlessControl9
title: IVMRWindowlessControl9
author: windows-sdk-content
description: The IVMRWindowlessControl9 interface controls how the Video Mixing Renderer Filter 9 (VMR-9) renders a video stream within a container window.
old-location: dshow\ivmrwindowlesscontrol9.htm
tech.root: DirectShow
ms.assetid: 9db99c31-65b5-4ff1-9c0d-22140a3687e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRWindowlessControl9, IVMRWindowlessControl9 interface [DirectShow], IVMRWindowlessControl9 interface [DirectShow],described, IVMRWindowlessControl9Interface, dshow.ivmrwindowlesscontrol9, vmr9/IVMRWindowlessControl9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRWindowlessControl9 interface


## -description



The <b>IVMRWindowlessControl9</b> interface controls how the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9) renders a video stream within a container window. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRWindowlessControl9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRWindowlessControl9</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd390538(v=VS.85).aspx">DisplayModeChanged</a>
</td>
<td align="left" width="63%">
Informs the VMR that a <a href="https://msdn.microsoft.com/5a6111fd-648e-41a9-aaf8-e5d93f5d54cd">WM_DISPLAYCHANGE</a> message has been received by the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390539(v=VS.85).aspx">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Retrieves the current aspect ratio display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390540(v=VS.85).aspx">GetBorderColor</a>
</td>
<td align="left" width="63%">
Retrieves the current border color used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390541(v=VS.85).aspx">GetCurrentImage</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the current image being displayed by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390542(v=VS.85).aspx">GetMaxIdealVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum video size that the VMR can display without incurring significant performance or image quality degradation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390543(v=VS.85).aspx">GetMinIdealVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the minimum video size that the VMR can display without incurring significant performance or image quality degradation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390544(v=VS.85).aspx">GetNativeVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the un-stretched video size and aspect ratio of the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390545(v=VS.85).aspx">GetVideoPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current source and destination rectangles used to display the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390546(v=VS.85).aspx">RepaintVideo</a>
</td>
<td align="left" width="63%">
Repaints the current video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390547(v=VS.85).aspx">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Sets the current aspect ratio display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390548(v=VS.85).aspx">SetBorderColor</a>
</td>
<td align="left" width="63%">
Sets the border color to be used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390549(v=VS.85).aspx">SetVideoClippingWindow</a>
</td>
<td align="left" width="63%">
Specifies the container window that video should be clipped to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390550(v=VS.85).aspx">SetVideoPosition</a>
</td>
<td align="left" width="63%">
Sets the source and destination rectangles for the video.

</td>
</tr>
</table> 


## -remarks



The VMR-9 supports this interface in windowless and renderless modes only. In windowed mode, <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> returns <b>E_NOINTERFACE</b>. For more information, see <a href="https://msdn.microsoft.com/98244af1-5934-4d1c-b9c3-7a414b065fe7">VMR Modes of Operation</a>.

Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

