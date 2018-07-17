---
UID: NN:strmif.IVMRMixerControl
title: IVMRMixerControl
author: windows-sdk-content
description: The IVMRMixerControl interface is enables an application to manipulate the incoming video streams on the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrmixercontrol.htm
old-project: DirectShow
ms.assetid: 2aefaebc-14e7-4918-9256-c5e9e3449095
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IVMRMixerControl, IVMRMixerControl interface [DirectShow], IVMRMixerControl interface [DirectShow],described, IVMRMixerControlInterface, dshow.ivmrmixercontrol, strmif/IVMRMixerControl
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMixerControl interface


## -description



The <code>IVMRMixerControl</code> interface is enables an application to manipulate the incoming video streams on the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7). Although this interface is implemented on the filter, it is actually the mixer component that is being configured. For this reason, this interface is only available when the mixer has been loaded through a call to <a href="https://msdn.microsoft.com/cd200b33-bb74-474a-9047-d81cb470af23">IVMRFilterConfig::SetNumberOfStreams</a>. This interface is intended for use by applications only; it should not be used by upstream filters.

For the VMR-9, use the <a href="https://msdn.microsoft.com/f311303a-8270-40b6-8153-e0bd8b232c69">IVMRMixerControl9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRMixerControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRMixerControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRMixerControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0a82a8f-a03a-43d7-8fb0-4c15b0cb7c27">GetAlpha</a>
</td>
<td align="left" width="63%">
Retrieves the constant alpha value that is applie to this video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/095f0ed3-46e4-48f9-97d5-5bca1c2efa30">GetBackgroundClr</a>
</td>
<td align="left" width="63%">
Retrieves the background color of the output rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee410a7e-e021-408a-bf40-cb58dc8eca1c">GetMixingPrefs</a>
</td>
<td align="left" width="63%">
Retrieves the mixing preferences for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da6409b0-161d-4724-b448-e68cb5d1941c">GetOutputRect</a>
</td>
<td align="left" width="63%">
Retrieves the position of this stream's video rectangle within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76f84c77-e528-4059-8f40-5e49db9ec567">GetZOrder</a>
</td>
<td align="left" width="63%">
Retrieves this video stream's position in the Z order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aab95d45-b8f1-40cb-811f-c1d00aa37c97">SetAlpha</a>
</td>
<td align="left" width="63%">
Sets a constant alpha value that is applied to this video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f163f62a-8d2b-43af-bec1-cae67a9747b7">SetBackgroundClr</a>
</td>
<td align="left" width="63%">
Sets the background color of the output rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7e1689c-03b4-457e-8d4c-6d59a70c42af">SetMixingPrefs</a>
</td>
<td align="left" width="63%">
Sets the mixing preferences for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7e1689c-03b4-457e-8d4c-6d59a70c42af">SetOutputRect</a>
</td>
<td align="left" width="63%">
Sets the position of this stream within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1ef562e-049c-4edf-a83c-76675e2113c6">SetZOrder</a>
</td>
<td align="left" width="63%">
Sets this video stream's position in the Z-order.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

