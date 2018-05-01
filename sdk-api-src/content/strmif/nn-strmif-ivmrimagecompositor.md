---
UID: NN:strmif.IVMRImageCompositor
title: IVMRImageCompositor
author: windows-driver-content
description: The IVMRImageCompositor interface is implemented by the default compositor for the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrimagecompositor.htm
old-project: DirectShow
ms.assetid: d905e871-c156-4140-bb3f-a19fa0cd79be
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IVMRImageCompositor, IVMRImageCompositor interface [DirectShow], IVMRImageCompositor interface [DirectShow], described, IVMRImageCompositorInterface, dshow.ivmrimagecompositor, strmif/IVMRImageCompositor
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IVMRImageCompositor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRImageCompositor interface


## -description



The <code>IVMRImageCompositor</code> interface is implemented by the default compositor for the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7). It must also be implemented by any plug-in compositor that an application provides for the VMR-7. The VMR-7 calls the methods on this interface to inform the Compositor that it should composite the incoming video frames into a single output frame. Applications do not use this interface.

For the VMR-9, use the <a href="https://msdn.microsoft.com/19fda7f2-000f-47d0-a7c7-d8421de418a2">IVMRImageCompositor9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRImageCompositor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRImageCompositor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRImageCompositor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5af73543-d391-404a-9797-8fbb3f24879c">CompositeImage</a>
</td>
<td align="left" width="63%">
Composites the current frames available in each input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16d54090-a0fa-480f-ba94-a15aa08d4576">InitCompositionTarget</a>
</td>
<td align="left" width="63%">
Informs the compositor that a new composition target has been created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea3ed291-d837-4d11-bc82-0a060b093b21">SetStreamMediaType</a>
</td>
<td align="left" width="63%">
Sets the media type for the input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9526be0-06aa-4fe3-ba05-fbac01806ec4">TermCompositionTarget</a>
</td>
<td align="left" width="63%">
Informs the compositor that the current composition target is being replaced.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

