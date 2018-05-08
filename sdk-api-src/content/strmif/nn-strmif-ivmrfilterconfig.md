---
UID: NN:strmif.IVMRFilterConfig
title: IVMRFilterConfig
author: windows-driver-content
description: The IVMRFilterConfig interface is used to configure the operating mode and video rendering mechanisms of the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrfilterconfig.htm
old-project: DirectShow
ms.assetid: 3ea7bb41-1f5f-496f-bdf4-776ec9f28876
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IVMRFilterConfig, IVMRFilterConfig interface [DirectShow], IVMRFilterConfig interface [DirectShow],described, IVMRFilterConfigInterface, dshow.ivmrfilterconfig, strmif/IVMRFilterConfig
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
-	IVMRFilterConfig
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRFilterConfig interface


## -description



The <code>IVMRFilterConfig</code> interface is used to configure the operating mode and video rendering mechanisms of the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7). For the VMR-9, use the <a href="https://msdn.microsoft.com/089e44c8-6a27-410d-aad5-08816bd4f915">IVMRFilterConfig9</a> interface.

Applications must add the VMR to the graph and configure it before connecting it to any upstream filters (for example, in a call to <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a>). Once a filter has been connected to the VMR, the VMR's configuration is locked and all future attempts to alter it fail.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRFilterConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRFilterConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRFilterConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e031c427-23bb-4243-bb38-0837a6db8c2c">GetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Retrieves the number of input streams being mixed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/139b0326-2ab1-4fa4-91ae-9115b4368660">GetRenderingMode</a>
</td>
<td align="left" width="63%">
Retrieves the rendering mode currently being used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aabf3628-3179-430c-a74b-0cb4e552cbe2">GetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Retrieves the current set of rendering preferences being used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/504380d4-4df6-4b01-8db3-5c769a3d4106">SetImageCompositor</a>
</td>
<td align="left" width="63%">
Installs an application-provided image compositor object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd200b33-bb74-474a-9047-d81cb470af23">SetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Sets the number of streams to be mixed and instructs the VMR to go into mixer mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11fbc818-b0c3-4ce1-b9fe-7e4ba1f81467">SetRenderingMode</a>
</td>
<td align="left" width="63%">
Sets the rendering mode used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1374d071-f396-4fcb-8ca2-ac3986960207">SetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Sets various application preferences related to video rendering.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

