---
UID: NN:segment.IMSVidVideoRenderer2
title: IMSVidVideoRenderer2
author: windows-sdk-content
description: The IMSVidVideoRenderer2 interface represents a video renderer device.
old-location: mstv\imsvidvideorenderer2.htm
tech.root: mstv
ms.assetid: caaa2cf1-15be-47dc-82db-06915a55ba03
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidVideoRenderer2, IMSVidVideoRenderer2 interface [Microsoft TV Technologies], IMSVidVideoRenderer2 interface [Microsoft TV Technologies],described, IMSVidVideoRenderer2Interface, mstv.imsvidvideorenderer2, segment/IMSVidVideoRenderer2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRenderer2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer2 interface


## -description



The <b>IMSVidVideoRenderer2</b> interface represents a video renderer device. The <a href="https://msdn.microsoft.com/ffb9566f-1c03-4aba-a9ce-a47e42894ca0">MSVidVideoRenderer</a> object exposes this interface.

This interface provides access to the Video Mixing Renderer (VMR) filter. It inherits the <a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a> interface and adds support for custom allocator-presenters.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidVideoRenderer2</b> interface inherits from <a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a>. <b>IMSVidVideoRenderer2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidVideoRenderer2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c73edfea-bafd-4640-9be6-45e5a2bb81ef">_SetAllocator</a>
</td>
<td align="left" width="63%">
Specifies an allocator-presenter for the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b22d643e-f458-4293-9f2b-e8bfe1499905">get__Allocator</a>
</td>
<td align="left" width="63%">
Retrieves the allocator-presenter from the VMR

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ba2c9ba-c3ba-4095-8221-a424776f3fac">get_Allocator</a>
</td>
<td align="left" width="63%">
Retrieves the allocator-presenter from the VMR as an <b>IUnknown</b> pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d512525-ed18-43af-9773-ed56c49c3641">get_Allocator_ID</a>
</td>
<td align="left" width="63%">
Retrieves an identifier for the VMR filter's allocator-presenter

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a8546f8-61de-4e98-bee3-26ca4d0ea2e4">get_SuppressEffects</a>
</td>
<td align="left" width="63%">
Retrieves settings that control power management and visual effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d362addb-626a-42f8-9b95-82189a338527">put_SuppressEffects</a>
</td>
<td align="left" width="63%">
Sets preferences for power management and visual effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c73edfea-bafd-4640-9be6-45e5a2bb81ef">SetAllocator</a>
</td>
<td align="left" width="63%">
Specifies an allocator-presenter for the VMR as an <b>IUnknown</b> pointer.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVideoRenderer2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

