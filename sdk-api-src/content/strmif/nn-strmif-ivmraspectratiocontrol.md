---
UID: NN:strmif.IVMRAspectRatioControl
title: IVMRAspectRatioControl (strmif.h)
author: windows-sdk-content
description: The IVMRAspectRatioControl interface controls whether the Video Mixing Renderer Filter 7 (VMR-7) preserves the aspect ratio of the source video.
old-location: dshow\ivmraspectratiocontrol.htm
tech.root: DirectShow
ms.assetid: a341be9d-9801-4215-840d-7d581e9ec3cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRAspectRatioControl, IVMRAspectRatioControl interface [DirectShow], IVMRAspectRatioControl interface [DirectShow],described, IVMRAspectRatioControlInterface, dshow.ivmraspectratiocontrol, strmif/IVMRAspectRatioControl
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
 - IVMRAspectRatioControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRAspectRatioControl interface


## -description



The <code>IVMRAspectRatioControl</code> interface controls whether the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7) preserves the aspect ratio of the source video. This interface is available when the VMR-7 is operating in either windowed or windowless modes. In windowless mode, the same functionality is provided by the <a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRAspectRatioControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRAspectRatioControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRAspectRatioControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/baecb2a1-e7d8-43ee-ac7d-d2dcf50cb594">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Queries whether the VMR will preserve the aspect ratio of the source video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e73362ea-b153-4d25-b30e-c69274b49bf9">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Specifies whether the VMR will preserve the aspect ratio of the source video.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

