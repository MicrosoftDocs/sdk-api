---
UID: NN:vmr9.IVMRImagePresenter9
title: IVMRImagePresenter9 (vmr9.h)
author: windows-sdk-content
description: The IVMRImagePresenter9 interface is implemented by the default allocator-presenter for the Video Mixing Renderer Filter 9 (VMR-9).
old-location: dshow\ivmrimagepresenter9.htm
tech.root: DirectShow
ms.assetid: 2c18cdd6-af97-4db2-80b5-bab4cfa25f7d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRImagePresenter9, IVMRImagePresenter9 interface [DirectShow], IVMRImagePresenter9 interface [DirectShow],described, IVMRImagePresenter9Interface, dshow.ivmrimagepresenter9, vmr9/IVMRImagePresenter9
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
 - IVMRImagePresenter9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRImagePresenter9 interface


## -description



The <code>IVMRImagePresenter9</code> interface is implemented by the default allocator-presenter for the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9). It must also be implemented by any plug-in allocator-presenter that an application provides for the VMR-9. The VMR-9 uses this interface to inform the allocator-presenter that it should present the video frame contained in the supplied Direct3D surface. Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRImagePresenter9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRImagePresenter9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRImagePresenter9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377392(v=VS.85).aspx">PresentImage</a>
</td>
<td align="left" width="63%">
Called at precisely the moment this video frame should be presented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377393(v=VS.85).aspx">StartPresenting</a>
</td>
<td align="left" width="63%">
Called just before the video starts playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377394(v=VS.85).aspx">StopPresenting</a>
</td>
<td align="left" width="63%">
Called just after the video stops playing.

</td>
</tr>
</table> 


## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

