---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
<a href="https://msdn.microsoft.com/0806f27c-4728-4492-a2ac-26067b7c0aaa">GetAlpha</a>
</td>
<td align="left" width="63%">
Retrieves the constant alpha value that is applied to this video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1be2fb34-b0f3-4dff-8813-a487229af6dc">GetBackgroundClr</a>
</td>
<td align="left" width="63%">
Retrieves the background color of the output rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25df0310-124a-48a5-b0fc-bea1dfd35781">GetMixingPrefs</a>
</td>
<td align="left" width="63%">
Retrieves the mixing preferences for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93d976a4-1c48-4aac-8326-92b1ad9b751c">GetOutputRect</a>
</td>
<td align="left" width="63%">
Retrieves the position of this stream's video rectangle within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f100a5b-48d1-40cc-b4ab-02245afde550">GetProcAmpControl</a>
</td>
<td align="left" width="63%">
Retrieves the current image adjustment settings, such as brightness, contrast, hue, and saturation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7db2b22-b3d2-4c6f-84fc-5a287761ed7a">GetProcAmpControlRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for an image adjustment setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eccc72cc-9ae5-45e9-a47a-5dddc901d1b5">GetZOrder</a>
</td>
<td align="left" width="63%">
Retrieves this video stream's position in the Z-order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c746d473-bfa4-403c-8775-3f7270836a73">SetAlpha</a>
</td>
<td align="left" width="63%">
Sets a constant alpha value that is applied to this video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fed7f4bb-519c-4e02-be99-065b9131e57c">SetBackgroundClr</a>
</td>
<td align="left" width="63%">
Sets the background color of the output rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db5bf775-685c-4137-846d-fe71cddce08d">SetMixingPrefs</a>
</td>
<td align="left" width="63%">
Sets the mixing preferences for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d09d2e90-e121-46e0-a659-e7bae4432031">SetOutputRect</a>
</td>
<td align="left" width="63%">
Sets the position of this stream within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e2949f5-87e5-4748-bb23-be14452c8c82">SetProcAmpControl</a>
</td>
<td align="left" width="63%">
Sets the image adjustment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbc847d4-5d93-4994-b5f4-d753a528532a">SetZOrder</a>
</td>
<td align="left" width="63%">
Sets this video stream's position in the Z-order.

</td>
</tr>
</table> 


## -remarks



The VMR-9 supports this interface in mixing mode only. To enable mixing mode, call <a href="https://msdn.microsoft.com/062aac78-6d7d-4335-963a-bc2c2d339efb">IVMRFilterConfig9::SetNumberOfStreams</a>. Otherwise, <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> returns <b>E_NOINTERFACE</b>. 


        Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

