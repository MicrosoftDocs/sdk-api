---
UID: NN:vmr9.IVMRFilterConfig9
title: IVMRFilterConfig9
author: windows-sdk-content
description: The IVMRFilterConfig9 interface is implemented by the Video Mixing Renderer Filter 9.
old-location: dshow\ivmrfilterconfig9.htm
old-project: DirectShow
ms.assetid: 089e44c8-6a27-410d-aad5-08816bd4f915
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVMRFilterConfig9, IVMRFilterConfig9 interface [DirectShow], IVMRFilterConfig9 interface [DirectShow],described, IVMRFilterConfig9Interface, dshow.ivmrfilterconfig9, vmr9/IVMRFilterConfig9
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: VMR9DeinterlaceTech
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRFilterConfig9
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRFilterConfig9 interface


## -description



The <code>IVMRFilterConfig9</code> interface is implemented by the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a>. Applications use this interface to configure the VMR's operating mode and video rendering mechanisms. Applications must add the VMR to the graph and configure it before it is connected to any upstream filters (for example, in a call to <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a>). Once a filter has been connected to the VMR, the VMR's configuration is locked and all future attempts to alter it fail.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRFilterConfig9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRFilterConfig9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRFilterConfig9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34b26c3a-ac5d-479e-ac9d-c782cd5dded8">GetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Retrieves the number of input streams being mixed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e39077ce-737f-4dd9-ab7d-4dc087828fdf">GetRenderingMode</a>
</td>
<td align="left" width="63%">
Retrieves the rendering mode currently being used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b82a9dbe-aa86-4153-945b-fe8968faa5ca">GetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Retrieves the current set of rendering preferences being used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e4a66e8-d4ab-49e0-8773-c79b5965124b">SetImageCompositor</a>
</td>
<td align="left" width="63%">
Installs an application-provided image compositor object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/062aac78-6d7d-4335-963a-bc2c2d339efb">SetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Sets the number of streams to be mixed and instructs the VMR to go into mixer mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7a27d7c-5cd4-4a20-ba15-7056d502e3e3">SetRenderingMode</a>
</td>
<td align="left" width="63%">
Sets the rendering mode used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce274528-c759-4b43-80c7-0ba1e1275b7d">SetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Sets various application preferences related to video rendering.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

