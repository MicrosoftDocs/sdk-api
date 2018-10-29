---
UID: NN:strmif.IVMRWindowlessControl
title: IVMRWindowlessControl
author: windows-sdk-content
description: The IVMRWindowlessControl interface controls how the Video Mixing Renderer Filter 7 (VMR-7) renders a video stream within a container window.
old-location: dshow\ivmrwindowlesscontrol.htm
tech.root: DirectShow
ms.assetid: c21c5611-f376-4899-9914-c14a18af3810
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IVMRWindowlessControl, IVMRWindowlessControl interface [DirectShow], IVMRWindowlessControl interface [DirectShow],described, IVMRWindowlessControlInterface, dshow.ivmrwindowlesscontrol, strmif/IVMRWindowlessControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IVMRWindowlessControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRWindowlessControl interface


## -description



The <code>IVMRWindowlessControl</code> interface controls how the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7) renders a video stream within a container window. Applications must first put the VMR-7 into windowless mode before using this interface.

For the VMR-9, use the <a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRWindowlessControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRWindowlessControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRWindowlessControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83fbca03-0e8c-4386-96ff-f572f0b13312">DisplayModeChanged</a>
</td>
<td align="left" width="63%">
Informs the VMR that a WM_DISPLAYCHANGE message has been received by the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/452837f9-e910-4e6b-8552-9da29a6b63f1">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Queries whether the VMR will preserve the aspect ratio of the source video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0bf04c8-17e6-4e1f-b35f-2e10c9de8b92">GetBorderColor</a>
</td>
<td align="left" width="63%">
Retrieves the current border color used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e10f9e03-fbcd-4002-babc-fb028e399d72">GetColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the current source color key value used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/515e252d-4ac4-49ec-8d94-bf850dd4783f">GetCurrentImage</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the current image being displayed by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cfd8c4e-70e0-4a7e-a47e-4ad0535e5cb2">GetMaxIdealVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum video size that the VMR can display without incurring significant performance or image quality degradation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/602e32d4-41d6-4139-aa64-4b53caa50859">GetMinIdealVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the minimum video size that the VMR can display without incurring significant performance or image quality degradation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc8fd96d-e9a8-4911-9330-a4cf71a2d926">GetNativeVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the un-stretched video size and aspect ratio of the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d7f1a8b-bbc4-43ae-b8e6-410561087204">GetVideoPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current source and destination rectangles used to display the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16ef3bc1-1781-44f7-a997-ae9b1b3c405c">RepaintVideo</a>
</td>
<td align="left" width="63%">
Repaints the current video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/421910fb-8007-4347-a57c-6a46b7b733b3">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will preserve the aspect ratio of the source video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d58ce18f-ddc4-4d91-b086-8829056f4508">SetBorderColor</a>
</td>
<td align="left" width="63%">
Sets the border color to be used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9facf4af-ed56-4a94-b351-35ddd7f63e6e">SetColorKey</a>
</td>
<td align="left" width="63%">
Sets the source color key value that the VMR should use

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82589745-8f79-4e0e-b28c-5a395390ba64">SetVideoClippingWindow</a>
</td>
<td align="left" width="63%">
Specifies the container window that video should be clipped to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cf75b8e-850d-4514-9502-a71c801e0d92">SetVideoPosition</a>
</td>
<td align="left" width="63%">
Sets the source and destination rectangles for the video.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

