---
UID: NN:vmr9.IVMRAspectRatioControl9
title: IVMRAspectRatioControl9
author: windows-driver-content
description: The IVMRAspectRatioControl9 interface controls whether the Video Mixing Renderer Filter 9 (VMR-9) preserves the aspect ratio of the source video.
old-location: dshow\ivmraspectratiocontrol9.htm
old-project: DirectShow
ms.assetid: ae850eea-c283-4500-baa0-e26641576852
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IVMRAspectRatioControl9, IVMRAspectRatioControl9 interface [DirectShow], IVMRAspectRatioControl9 interface [DirectShow],described, IVMRAspectRatioControl9Interface, dshow.ivmraspectratiocontrol9, vmr9/IVMRAspectRatioControl9
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
-	IVMRAspectRatioControl9
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRAspectRatioControl9 interface


## -description



The <code>IVMRAspectRatioControl9</code> interface controls whether the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9) preserves the aspect ratio of the source video. This interface is available when the VMR is operating in either windowed or windowless modes. In windowless mode, the same functionality is provided by the <a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRAspectRatioControl9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRAspectRatioControl9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRAspectRatioControl9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e53e9015-5186-4807-a5ee-af8598a89a2b">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Queries whether the VMR will preserve the aspect ratio of the source video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adc34013-a349-4cf6-b5c2-58b7b212d630">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will preserve the aspect ratio of the source video.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

