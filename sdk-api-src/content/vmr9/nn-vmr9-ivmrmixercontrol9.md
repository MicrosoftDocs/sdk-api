---
UID: NN:vmr9.IVMRMixerControl9
title: IVMRMixerControl9 (vmr9.h)
author: windows-sdk-content
description: The IVMRMixerControl9 interface enables an application to manipulate the incoming video streams on the Video Mixing Renderer Filter 9 (VMR-9). This interface is intended for use by applications only; it should not be used by upstream filters.
old-location: dshow\ivmrmixercontrol9.htm
tech.root: DirectShow
ms.assetid: f311303a-8270-40b6-8153-e0bd8b232c69
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRMixerControl9, IVMRMixerControl9 interface [DirectShow], IVMRMixerControl9 interface [DirectShow],described, IVMRMixerControl9Interface, dshow.ivmrmixercontrol9, vmr9/IVMRMixerControl9
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
 - IVMRMixerControl9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMixerControl9 interface


## -description



The <b>IVMRMixerControl9</b> interface enables an application to manipulate the incoming video streams on the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9). This interface is intended for use by applications only; it should not be used by upstream filters.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRMixerControl9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRMixerControl9</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd390458(v=VS.85).aspx">GetAlpha</a>
</td>
<td align="left" width="63%">
Retrieves the constant alpha value that is applied to this video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390459(v=VS.85).aspx">GetBackgroundClr</a>
</td>
<td align="left" width="63%">
Retrieves the background color of the output rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390460(v=VS.85).aspx">GetMixingPrefs</a>
</td>
<td align="left" width="63%">
Retrieves the mixing preferences for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390461(v=VS.85).aspx">GetOutputRect</a>
</td>
<td align="left" width="63%">
Retrieves the position of this stream's video rectangle within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390462(v=VS.85).aspx">GetProcAmpControl</a>
</td>
<td align="left" width="63%">
Retrieves the current image adjustment settings, such as brightness, contrast, hue, and saturation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390463(v=VS.85).aspx">GetProcAmpControlRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for an image adjustment setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390464(v=VS.85).aspx">GetZOrder</a>
</td>
<td align="left" width="63%">
Retrieves this video stream's position in the Z-order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390465(v=VS.85).aspx">SetAlpha</a>
</td>
<td align="left" width="63%">
Sets a constant alpha value that is applied to this video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390466(v=VS.85).aspx">SetBackgroundClr</a>
</td>
<td align="left" width="63%">
Sets the background color of the output rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390467(v=VS.85).aspx">SetMixingPrefs</a>
</td>
<td align="left" width="63%">
Sets the mixing preferences for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390468(v=VS.85).aspx">SetOutputRect</a>
</td>
<td align="left" width="63%">
Sets the position of this stream within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390469(v=VS.85).aspx">SetProcAmpControl</a>
</td>
<td align="left" width="63%">
Sets the image adjustment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390470(v=VS.85).aspx">SetZOrder</a>
</td>
<td align="left" width="63%">
Sets this video stream's position in the Z-order.

</td>
</tr>
</table> 


## -remarks



The VMR-9 supports this interface in mixing mode only. To enable mixing mode, call <a href="https://msdn.microsoft.com/en-us/library/Dd377370(v=VS.85).aspx">IVMRFilterConfig9::SetNumberOfStreams</a>. Otherwise, <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> returns <b>E_NOINTERFACE</b>. 

Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

