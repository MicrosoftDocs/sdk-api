---
UID: NN:vmr9.IVMRImagePresenterConfig9
title: IVMRImagePresenterConfig9
author: windows-sdk-content
description: The IVMRImagePresenterConfig interface provides methods for setting the renderering preferences on the allocator-presenter used by the Video Mixing Renderer Filter 9 (VMR-9).Applications should not use this interface directly.
old-location: dshow\ivmrimagepresenterconfig9.htm
tech.root: DirectShow
ms.assetid: fc3c9b4d-0213-47d5-96e4-db582c80ca4e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRImagePresenterConfig9, IVMRImagePresenterConfig9 interface [DirectShow], IVMRImagePresenterConfig9 interface [DirectShow],described, IVMRImagePresenterConfig9Interface, dshow.ivmrimagepresenterconfig9, vmr9/IVMRImagePresenterConfig9
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
 - IVMRImagePresenterConfig9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRImagePresenterConfig9 interface


## -description



The <a href="https://msdn.microsoft.com/en-us/library/Dd377395(v=VS.85).aspx">IVMRImagePresenterConfig</a> interface provides methods for setting the renderering preferences on the allocator-presenter used by the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9).

Applications should not use this interface directly. The VMR-9 filter's <a href="https://msdn.microsoft.com/en-us/library/Dd377365(v=VS.85).aspx">IVMRFilterConfig9</a> interface calls methods on this interface. The default allocator-presenter implements this interface. Custom allocator-presenters can also expose this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRImagePresenterConfig9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRImagePresenterConfig9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRImagePresenterConfig9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377397(v=VS.85).aspx">GetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Gets the rendering preferences.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377398(v=VS.85).aspx">SetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Sets the rendering preferences.

</td>
</tr>
</table> 


## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

